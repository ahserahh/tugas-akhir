# OTS
Aplikasi Ujian Pilihan Ganda Online

## Kebutuhan Server

Aplikasi ini dibangun diatas Framework <a href="https://laravel.com/docs/5.5" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">Laravel 5.4</a> dan MySQL versi 5. Sebelum menjalankan aplikasi ini, silahkan disiapkan terlebih dahulu beberapa software dan ekstension berikut:

- PHP versi 7.1.0 keatas
  - OpenSSL PHP Extension
  - PDO PHP Extension
  - Mbstring PHP Extension
  - Tokenizer PHP Extension
  - XML PHP Extension
- MySQL
- Browser (lebih direkomendasikan Chrome versi 60 keatas

## Instalasi

Disini akan saya jelaskan proses instalasi pada sistem operasi Windows.

Pertama silahkan download XAMPP, silahkan download <a href="https://www.apachefriends.org/xampp-files/7.0.32/xampp-win32-7.0.32-0-VC14-installer.exe" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.
Silahkan install XAMPP yang telah berhasil Anda download. Pastikan dikomputer Anda belum terinstall PHP & MySQL untuk menghindari konflik port. Apabila sebelumnya telah ada, silahkan cek versi PHP harus 7.1 atau 7.2.

Setelah berhasil menginstal PHP dan MySQL (dalam paket XAMPP), kita lanjutkan install composer dan gitbash.

Untuk composer silahkan download <a href="https://getcomposer.org/" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.

Untuk gitbash silahkan download <a href="https://git-scm.com/download/win" target="_blank" title="silahkan buka di tab baru, dengan klik kanan atau klik CTRL + clik">disini</a>.

Silahkan instal composer dan git bash di komputer server Anda. Setelah semua berhasil diinstal dengan benar kita bisa mulai clone aplikasi ini ke komputer kita.

Buka command prompt (gitbash) lalu arahkan ke folder htdocs (ada didalam folder xampp, misal Anda menginstal di C. Berarti Anda harus ke folder C:\\xampp\htdocs).

Setelah itu ketikan:
```
https://github.com/ahserahh/tugas-akhir
```

Tunggu sampai file selesai di clone ke folder htdocs server Anda, lalu masuk ke folder <b>tugas-akhir</b> dengan mengetikan (```cd tugas-akhir```) pada command prompt (gitbash) Anda, lalu ketikan :

```
composer install
php artisan key:generate
```

Atau apabila anda telah melakukan instalasi sebelumnya silahkan update composer dengan ketikan script dibawah ini (opsi ini hanya digunakan apabila terdapat update aplikasi, saat instalasi awal tidak diperlukan menggunakan script ini karena akan memakan waktu cukup lama):

```
composer update --verbose --profile --prefer-dist
```

Buka browser dan ketikan url http://localhost/phpmyadmin. Lalu buat database baru dengan nama <b>ots</b>. Setelah itu ketikan script berikut pada command promt:
```
php artisan migrate
php artisan db:seed
```

Setelah proses diatas berhasil dilalui tanpa hambatan, silahkan akses di browser url http://localhost/ots/public untuk mengakses aplikasi ujian.

Untuk login sebagai guru silahkan gunakan email: <b>admin@admin.com</b>, password: <b>admin</b>
