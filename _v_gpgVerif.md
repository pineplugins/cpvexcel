# Verify File Signature with GPG (.asc / .sig)

When downloading software such as .tar.gz, .zip, or .whl, you may also get a .asc or .sig signature file. This file is useful for verifying that the file comes from an official source and has not been modified.

What is GPG Verification?

GPG (GNU Privacy Guard) uses public key cryptography to verify:
1. Authenticity – The file came from the original creator.
2. Integrity – The file has not been modified since it was signed.

3. Download the required files

For example:
- cpvx-1.0.1.tar.gz
- cpvx-1.0.1.tar.gz.asc ← detached signature

2. Import Public Key

a. Via keyserver:

```term
$ gpg --keyserver keyserver.ubuntu.com --recv-keys 0xABCDEF1234567890
$ Output if successful:
gpg: key ABCDEF1234567890: public key "Developer Name <dev@example.com>" imported
gpg: Total number processed: 1
gpg: imported: 1
$ If it has already been imported:
gpg: key ABCDEF1234567890: "Developer Name <dev@example.com>" not changed
gpg: Total number processed: 1
gpg: unchanged: 1
$ If failed:
gpg: keyserver receive failed: Data no
$ Or:
gpg: keyserver receive failed: Connection timed out
```

b. Import from local .asc file:

```term
$ gpg --import public-key.asc
$ Output if successful:
gpg: key ABCDEF1234567890: public key "Developer Name <dev@example.com>" imported
gpg: Total number processed: 1
gpg: imported: 1
$ If the file is not found:
gpg: can't open 'public-key.asc': No such file or directory
gpg: Total number processed: 0
$ If the file is damaged:
gpg: no valid OpenPGP data found.
gpg: Total number processed: 0
```

3. Signature Verification

Run:

```term
$ gpg --verify cpvx-1.0.1.tar.gz.asc cpvx-1.0.1.tar.gz
$ Possible Outputs and Their Meanings
$ A. Signature is valid and the key is trusted:
gpg: Signature made Fri 10 May 2025 04:21:30 PM UTC using RSA key ID ABCDEF1234567890
gpg: Good signature from "Developer Name <dev@example.com>"
$ Valid file, not modified.
$ B. Signature is valid, but key is not trusted:
gpg: Signature made Fri 10 May 2025 04:21:30 PM UTC using RSA key ID ABCDEF1234567890
gpg: Good signature from "Developer Name <dev@example.com>"
gpg: WARNING: This key is not certified with a trusted signature!
gpg: There is no indication that the signature belongs to the owner.
$ Signature is valid, but you have not marked this key as trusted.
$ Solution:
$ term
$ gpg --edit-key ABCDEF1234567890
gpg> trust
```

C. Signature mismatch / file modified:

```
gpg: Signature made ...
gpg: BAD signature from "Developer Name <dev@example.com>"
```

The file is probably modified or corrupted.

D. Signature file not found:

```
gpg: can't open 'cpvx-1.0.1.tar.gz.asc': No such file or directory
gpg: verify signatures failed: No such file or directory
```

Make sure the .asc file is in the same folder.

E. Main file not found:

```
gpg: cpvx-1.0.1.tar.gz: No such file or directory
gpg: verify signatures failed: No such file or directory
```

F. Public key not imported:

```
gpg: Signature made ...
gpg: Can't check signature: No public key
```

Solution:

```term
$ gpg --recv-keys 0xABCDEF1234567890
```

Fingerprint Verification (Optional)

To ensure the authenticity of the key, you can check the fingerprint:

```term
$ gpg --fingerprint ABCDEF1234567890
```

Example output:

```
pub rsa4096 2024-05-10 [SC]
ABCD EFGH 1234 5678 90AB CDEF 1234 5678 90AB CDEF
uid [ unknown] Developer Name <dev@example.com>
```

Match this fingerprint with the one displayed on the developer's official website.

Conclusion

* Use GPG to verify the authenticity & integrity of files.
* Always check the fingerprint and make sure the key comes from a trusted source.
* Avoid using files that fail to verify (BAD signature).

Note:
For maximum security: verify the SHA512 hash as well so as not to rely solely on the GPG signature.