# Praktikum 8 : Register, Authentication, dan Authorization

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Mengimplementasikan register
2. Mengimplementasikan authentication
3. Memahami fungsi token
4. Mengimplementasikan authorization

##

### Dasar Teori Praktikum ###
1. Authentication adalah proses untuk mengenali identitas dengan mekanisme pengasosiasian permintaan yang masuk dengan satu set kredensial pengidentifikasi. Kredensial yang diberikan akan dibandingkan dengan database informasi pengguna yang berwenang di dalam sistem operasi lokal atau server otentifikasi.
2. Token merupakan nilai yang digunakan untuk mendapatkan akses ke sumber daya yang dibatasi secara elektronik. Penggunaan token ditujukan pada web service yang tidak menyimpan state yang berkaitan dengan penggunaan aplikasi (stateless), seperti session.
3. Authorization merupakan proses pemberian hak istimewa yang dilakukan setelah proses authentication. Setelah pengguna diidentifikasi pada proses authentication, authorization akan memberikan hak istimewa dan tindakan yang diizinkan kepada pengguna yang ditentukan.
   
##

### Langkah Percobaan Praktikum ###

### A. Register

1. Memastikan telah terdapatnya table users yang berisikan kolom id, createdAt, updatedAt, name, email, dan password

<img width="807" alt="Screenshot 2023-12-03 063632" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/67f0cbfe-e4d7-45a9-b0d6-fd77d06a525a">

---

2. Memastikan telah terdapatnya file User.php pada folder app/Models

<img width="842" alt="Screenshot 2023-12-03 063850" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/afe1e6ff-d556-4f92-b08c-343ffe372da5">

---

3. Membuat File bernamakan “AuthController.php”, kemudian menambahkan sintaks sesuai dengan modul praktikum

<img width="824" alt="Screenshot 2023-12-03 063910" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3785f302-4856-474a-8124-0a148861b158">

---

4. Menambahkan sintaks pada baris 102 - 104 sesuai dengan modul praktikum pada File web.php dalam folder routes

<img width="907" alt="Screenshot 2023-12-03 063928" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d013142d-2043-40eb-b90f-60c76a0a4e9c">

---

5. Menjalankan aplikasi menggunakan postman dengan URL “http://localhost:8000/auth/register”, method “POST”, dan body ("name": "Scaramouche", "email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses berhasil dengan mengembalikan output terkait informasi status (Success), message (new user created), dan data user (name “Scaramouche”, email “scaramouche@fatui.org”, password, updated_at, created_at, dan id “3”)

<img width="688" alt="Screenshot 2023-12-03 063958" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1af52585-0a30-47af-87d3-802cc7e9ae61">

---

### B. Authentication

1. Menambahkan sintaks sesuai dengan modul praktikum pada File AuthController.php dalam folder app/Http/Controllers, yaitu function login

<img width="840" alt="Screenshot 2023-12-03 064017" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4bc5f61d-8d33-4040-b1ac-b5d764cfc698">

---

2. Menambahkan sintaks pada baris 106 - 109 sesuai dengan modul praktikum pada File web.php dalam folder app/Http/Controllers

<img width="922" alt="Screenshot 2023-12-03 064042" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/67841f80-13d4-474a-91f0-e9145787a7e3">

---

3. Menjalankan aplikasi menggunakan postman dengan URL “http://localhost:8000/auth/login”, method “POST”, dan body ("email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses berhasil dengan mengembalikan output terkait informasi status (Success), message (successfully login), dan data user (id “3”, created_at, updated_at, name “Scaramouche”,  email “scaramouche@fatui.org”, dan password)

<img width="689" alt="Screenshot 2023-12-03 064114" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1f03d623-4240-4baa-a78a-4aee5664d5d0">

---

### C. Token

1. Menjalankan perintah “php artisan make:migration add_column_token_to_users” untuk membuat migrasi baru
   
<img width="885" alt="Screenshot 2023-12-03 064134" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b7d223b1-fc79-4b18-96ea-679e86bc3378">

---

2. Menambahkan sintaks pada baris 15 dan 25 sesuai dengan modul praktikum pada File migration add_column_token_to_users.php
   
<img width="679" alt="Screenshot 2023-12-03 064156" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/905e56ac-fe0e-476f-bd1a-4db9e58ce0c1">

---

3. Menambahkan sintaks pada baris 17, yaitu atribut token di $fillable, sesuai dengan modul praktikum pada File User.php dalam folder app/Models
   
<img width="871" alt="Screenshot 2023-12-03 064212" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7cde9314-7ad4-481a-b4ba-b62a88490330">

---

4. Menambahkan sintaks pada baris 67 dan 68 sesuai dengan modul praktikum pada File AuthController.php dalam folder app/Http/Controllers
   
<img width="800" alt="Screenshot 2023-12-03 064231" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/26d88470-e842-4ac8-8627-b7f051561776">

---

5. Menjalankan perintah “php artisan migrate” untuk menjalankan migrasi terbaru
   
<img width="862" alt="Screenshot 2023-12-03 064248" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5fdd498a-a02d-4e85-81fe-e3b818bc3ad2">

---

6. Menjalankan aplikasi menggunakan postman dengan URL “http://localhost:8000/auth/login”, method “POST”, dan body ("email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses berhasil dengan mengembalikan output terkait informasi status (Success), message (successfully login), dan data user (id “1”, created_at, updated_at, name “Scaramouche”,  email “scaramouche@fatui.org”, password, dan token). Setelah mendapatkan output, salinlah token yang didapat ke notepad karena akan dilanjutkan pada proses selanjutnya

<img width="674" alt="Screenshot 2023-12-03 064324" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4a047c13-ace3-4a3a-b85f-95466b5be68d">

---

### D. Authorization

1. Membuat File bernamakan “Authorization.php” pada folder app/Http/Middleware, kemudian menambahkan sintaks sesuai dengan modul praktikum

<img width="744" alt="Screenshot 2023-12-03 064339" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/96a6240b-16bb-4214-8c45-3abc1002bcda">

---

2. Menambahkan sintaks pada baris 78 - 82 sesuai dengan modul praktikum pada File app.php dalam folder bootstrap
   
<img width="829" alt="Screenshot 2023-12-03 064354" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/029160a6-49d3-4b34-924c-e229100771f6">

---

3. Menambahkan sintaks pada baris 96 - 105, yaitu function home(), sesuai dengan modul praktikum pada File HomeController.php dalam folder app/Http/Controllers
   
<img width="829" alt="Screenshot 2023-12-03 064408" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/530884aa-fc9e-4704-bb0f-53dfd4f2bb01">

---

4. Menambahkan sintaks pada baris 84 - 86 sesuai dengan modul praktikum pada File web.php dalam folder routes
   
<img width="905" alt="Screenshot 2023-12-03 064445" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e473ea40-1b35-41d6-9a22-2a3a9f9a9b73">

---

5. Menjalankan aplikasi menggunakan postman dengan URL “http://localhost:8000/home”, method “GET”, dan headers (Accept “*/*”, Accept-Encoding “gzip, deflate, br”, Connection “keep-alive”, dan token). Terlihat pada gambar bahwa proses berhasil dengan mengembalikan output terkait informasi status (Success) dan message (Selamat datang Scaramouche)
   
<img width="641" alt="Screenshot 2023-12-03 064506" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f9293d3c-d21b-4b71-a9da-5862716af8e5">

---

### Kesimpulan Praktikum ###

1. Register:
- Memastikan tabel users sudah ada dengan beberapa kolom, seperti "id", "createdAt", "updatedAt", "name", "email", dan "password".
- Membuat model "User.php" dengan atribut $fillable, yang mencakup name, email, dan password.
- Membuat controller "AuthController.php" dengan fungsi "register()" yang memproses permintaan registrasi dan membuat user baru.
  
2. Authentication:
- Menambahkan fungsi "login()" pada "AuthController.php" untuk mengelola proses login.
- Melakukan perbandingan terkait password yang diterima dari permintaan dengan password hashed di database.
- Apabila proses login berhasil, sebuah token akan di-generate menggunakan fungsi "Str::random(36)" dan disimpan di atribut token pada model "User".

3. Token:
- Membuat migrasi baru "add_column_token_to_users" untuk menambahkan kolom token ke tabel "users".
- Menambahkan atribut token pada model "User.php" dalam atribut $fillable.
- Setelah login berhasil, token di-generate dan disimpan di dalam database untuk digunakan pada proses authorization.

4. Authorization:
- Membuat middleware "Authorization.php" untuk mengecek keberadaan dan kevalidan token.
- Menambahkan middleware pada file "bootstrap/app.php".
- Menambahkan fungsi "home()" pada "HomeController.php" untuk menampilkan pesan selamat datang setelah login.
- Mengaplikasikan middleware auth pada route "/home" untuk memastikan bahwa hanya user yang sudah login yang dapat mengaksesnya.
   
##
