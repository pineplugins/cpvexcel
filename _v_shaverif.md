# Verify File Integrity (.sha512)

It is important to verify the integrity of `.zip`, `.tar.gz`, or `.whl` files from `pnexcel-plugin` before using them. This ensures that the files were not corrupted during download and were not modified in an unauthorized manner.

## What is SHA512 Verification?

SHA512 is a cryptographic hash algorithm that produces a unique digital fingerprint of a file. If the hash of your local file matches the one provided in the `.sha512` file, then your file is verified to be authentic and unchanged.

---

## SHA512 Verification Steps

1. Download the release file and the corresponding `.sha512` file

Example:
- `cpvx-1.0.1.tar.gz`
- `cpvx-1.0.1.tar.gz.sha512`

2. Open a terminal and navigate to the directory where the files are located.

3. Run the following command:

```term
$ sha512sum cpvx-1.0.1.tar.gz
437d1a2c3d7e91b4e3c7a123456789abcdeffedcba9876543210ffeeddccbbaa123456789abcdef123456789abcdef12345678  cpvx-1.0.1.tar.gz
````

4. Compare the result with the contents of `cpvx-1.0.1.tar.gz.sha512`.

Example output:

```term
$ sha512sum cpvx-1.0.1.tar.gz
437d1a2c3d7e91b4e3c7a123456789abcdeffedcba9876543210ffeeddccbbaa123456789abcdef123456789abcdef12345678  cpvx-1.0.1.tar.gz
```

Check that the hash on the left matches exactly with the one in the `.sha512` file.

---

## Possible Outcomes

### A. File exists and hash matches:

* You will see a hash printed, and it will match the `.sha512` file.
* This confirms the file is authentic and safe to use.

### B. File exists but hash does not match:

* You will see a hash printed, but it does **not** match the `.sha512` file.
* This means the file may be corrupted or tampered with.
* Action: Do **not** use the file. Delete it and download it again from the official source.

### C. File does not exist:

* Output will be:

```term
sha512sum: cpvx-1.0.1.tar.gz: No such file or directory
```
* Action: Make sure the file exists and you are in the correct directory.

### D. .sha512 file missing:

* You will not be able to compare the output manually.
* Action: Download the corresponding `.sha512` file from the official release page.

---

## For Windows Users

If you are on Windows, you can use the built-in `CertUtil` utility:

```term
$ certutil -hashfile cpvx-1.0.1.tar.gz SHA512
SHA512 hash of cpvx-1.0.1.tar.gz:
437d1a2c3d7e91b4e3c7a123456789abcdeffedcba9876543210ffeeddccbbaa123456789abcdef123456789abcdef12345678
CertUtil: -hashfile command completed successfully.
```

Manually compare this hash with the `.sha512` file.

---

## Summary

Always verify your files using SHA512 before installing or running them. A mismatch means the file is not safe to use. Verification is a quick but critical step for ensuring software integrity.
