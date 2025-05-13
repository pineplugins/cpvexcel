Berikut adalah template **Markdown** (`README.md`) yang dapat Anda gunakan untuk memberikan panduan tentang cara memverifikasi **SHA-512** dan **GPG** signature untuk file Anda.

````markdown
# Panduan Memverifikasi SHA-512 dan GPG Tanda Tangan

## Verifikasi Tanda Tangan SHA-512

SHA-512 adalah salah satu algoritma hash kriptografi yang menghasilkan nilai hash sepanjang 512 bit. Untuk memverifikasi integritas file menggunakan SHA-512, Anda bisa mengikuti langkah-langkah berikut.

### 1. **Menghitung SHA-512 dari File**

Untuk menghitung SHA-512 dari file yang ingin Anda verifikasi, jalankan perintah berikut:

```bash
sha512sum <nama_file>
````

Contoh untuk file `cpvx-1.0.0.tar.gz`:

```bash
sha512sum cpvx-1.0.0.tar.gz
```

Ini akan menghasilkan hash yang tampak seperti ini:

```
3a3e76d276ed8b6bbf4c65f7ed238d17e080938b0754159a3a3b16c2839f7f5e23b7f9f80a96d86b8d5168b029e1efb381c7c1c15a42394f7cc678cfdd92738a  cpvx-1.0.0.tar.gz
```

### 2. **Verifikasi SHA-512 dengan Nilai Hash yang Diketahui**

Jika Anda memiliki file hash yang diketahui (misalnya, `cpvx-1.0.0.tar.gz.sha512`), Anda bisa memverifikasi file dengan perintah berikut:

```bash
sha512sum -c cpvx-1.0.0.tar.gz.sha512
```

Jika hash file cocok, Anda akan mendapatkan output seperti ini:

```
cpvx-1.0.0.tar.gz: OK
```

Jika hash tidak cocok, berarti file tersebut telah berubah atau rusak.

---

## Verifikasi GPG Tanda Tangan

### 1. **Menandatangani File dengan GPG**

Untuk menandatangani file menggunakan GPG, Anda bisa menggunakan perintah berikut:

```bash
gpg --default-key "<key_id>" --output <file>.sig --detach-sign <file>
```

Contoh:

```bash
gpg --default-key "83A744827B5F47F8144D0E55F377F8AF64B3D453" --output cpvx-1.0.0.tar.gz.sig --detach-sign cpvx-1.0.0.tar.gz
```

File tanda tangan yang dihasilkan adalah `cpvx-1.0.0.tar.gz.sig`.

### 2. **Memverifikasi Tanda Tangan GPG**

Untuk memverifikasi tanda tangan GPG pada file, jalankan perintah berikut:

```bash
gpg --verify <file>.sig <file>
```

Contoh:

```bash
gpg --verify cpvx-1.0.0.tar.gz.sig cpvx-1.0.0.tar.gz
```

### 3. **Hasil Verifikasi yang Berhasil**

Jika verifikasi berhasil, Anda akan mendapatkan output seperti ini:

```bash
gpg: Signature made Sat 01 May 2025 04:30:45 PM UTC using RSA key ID 83A744827B5F47F8144D0E55F377F8AF64B3D453
gpg: Good signature from "Nama Pengguna <email@example.com>" [ultimate]
```

### 4. **Hasil Verifikasi yang Gagal**

Jika verifikasi gagal (misalnya, file sudah dimodifikasi), Anda akan mendapatkan output seperti ini:

```bash
gpg: BAD signature from "Nama Pengguna <email@example.com>"
```

---

## Kesimpulan

* **SHA-512** digunakan untuk memverifikasi integritas file berdasarkan nilai hash yang dihitung.
* **GPG** digunakan untuk memverifikasi tanda tangan digital pada file, yang menjamin keaslian dan integritas file tersebut dengan menggunakan kunci publik.

```

Penjelasan lebih lanjut:
- **SHA-512** adalah algoritma hash yang digunakan untuk memastikan integritas file. Jika nilai hash file yang dihitung sama dengan nilai hash yang diketahui (biasanya disediakan dalam file `.sha512`), berarti file tersebut tidak diubah.
- **GPG** memastikan keaslian file dan bahwa file tersebut ditandatangani oleh pemilik kunci privat yang sah. Jika file tersebut dimodifikasi setelah tanda tangan, verifikasi akan gagal.
```
