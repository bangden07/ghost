# Ghost Blog & CDN Cloudinary - Railway

Ini merupakan contoh versi self-hosted dari [Ghost](https://ghost.org/) yang di deploy ke Railway. Secara internal menggunakan database MySQL untuk menyimpan data.

[![Deploy di Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2Fbangden07%2Fghost-cdn-railway&plugins=mysql&envs=CLOUDINARY_URL%2CMAILGUN_SMTP_LOGIN%2CMAILGUN_SMTP_PASSWORD&optionalEnvs=CLOUDINARY_URL%2CMAILGUN_SMTP_LOGIN%2CMAILGUN_SMTP_PASSWORD&CLOUDINARY_URLDesc=For+file+storage.+If+you+do+not+add+this%2C+your+images+won%27t+persist+between+deploys)

## ✨ Fitur

- Ghost
- CDN by Cloudinary
- MySQL

## 💁‍♀️ Cara Install dan Penggunaan

- Klik tombol **"Deploy di Railway"** 👆
- Tambahkan variabel env
  - Jika Anda tidak menambahkan variabel env `CLOUDINARY_URL`, gambar/file Anda tidak akan bertahan di antara penyebaran.
  - Tambahkan variabel `MAILGUN_SMTP_LOGIN` dan `MAILGUN_SMTP_PSWORD` jika Anda ingin mengundang pengguna ke panel admin Anda atau mengirim email ke pelanggan Anda ketika Anda mempublikasikan posting baru.

## 📝 Catatan

- Sistem File Railway adalah Efemeral itulah sebabnya setiap perubahan pada sistem file tidak bertahan di antara penyebaran. Inilah sebabnya, contoh ini menggunakan Cloudinary untuk penyimpanan.
- Batasan di atas juga mempengaruhi cara tema bekerja dengan Ghost, kami menggunakan skrip `bin/themes.sh` untuk menyalin tema setiap kali Anda menggunakannya. Dengan begitu, temanya selalu ada.
  - Untuk menambahkan tema, pertama tambahkan package sebagai dependency pada file `package.json` dan kemudian tambahkan ke daftar tema dalam file `bin/themes.sh`.
  - Jangan tambahkan tema langsung menggunakan Ghost UI, sepertinya berhasil tetapi akan rusak setiap kali Anda menggunakan aplikasi Anda lagi.

