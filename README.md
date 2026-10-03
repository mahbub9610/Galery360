# Galeri Mockup 360

Situs statis untuk GitHub Pages: galeri render 360° berkelompok dengan titik info material.

## Isi folder

- `index.html` — seluruh situs
- `data/accounts.json` — 4 akun (kata sandi tidak tersimpan di sini, hanya kunci yang terbungkus)
- `data/gallery.enc` — daftar grup, foto, dan titik material (terenkripsi)
- `data/p/` — foto 360 dan gambar kecilnya (terenkripsi)
- `.nojekyll` — agar GitHub Pages menyajikan file apa adanya

## Memasang di GitHub Pages

1. Buat repo baru di GitHub, lalu unggah semua isi folder ini (termasuk `.nojekyll` dan folder `data`).
2. Buka Settings → Pages. Pada "Build and deployment", pilih "Deploy from a branch", branch `main`, folder `/ (root)`, lalu Save.
3. Tunggu sekitar satu menit, lalu buka `https://NAMA-AKUN.github.io/NAMA-REPO/`.

## Agar akun pemilik bisa mengunggah dan mengedit

1. Di GitHub buka Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token.
2. Repository access: "Only select repositories", pilih repo galeri ini.
3. Permissions → Repository permissions → Contents: "Read and write".
4. Masuk ke situs sebagai pemilik, buka Pengaturan, isi nama akun, nama repo, branch, dan token, lalu tekan Sambungkan.

Token hanya tersimpan di browser tempat Anda mengisinya. Jangan bagikan token itu: siapa pun yang memegangnya bisa mengubah repo.

## Catatan

- Perubahan (grup, foto, titik, kata sandi) baru terlihat pengguna lain setelah GitHub Pages selesai memperbarui situs, biasanya sekitar satu menit.
- Batas ukuran foto 50 MB per file. GitHub menyarankan total repo di bawah 1 GB.
- Ganti kata sandi bawaan lewat Pengaturan sebelum mengunggah foto asli.
- Untuk mencoba di komputer sendiri, jalankan server lokal (misalnya `python -m http.server`) lalu buka `http://localhost:8000`. Membuka `index.html` langsung dari folder tidak akan berfungsi.
