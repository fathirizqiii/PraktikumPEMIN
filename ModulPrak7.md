# Praktikum 7 : Relasi One-to-Many dan Many-to-Many

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Memahami relasi dan foreign key
2. Mengimplementasikan relasi one-to-many
3. Mengimplementasikan relasi many-to-many

##

### Dasar Teori Praktikum ###
1. Relasi merupakan hubungan antar tabel yang dilakukan dengan pencocokan primary key dengan foreign key untuk mengombinasikan data dari satu tabel dengan tabel lainnya.
2. Foreign Key merupakan properti yang digunakan untuk menandai hubungan dua tabel atau lebih. Foreign key pada tabel anak (child) akan menunjuk tabel induk (parent) yang menjadi referensinya (reference).
3. One-to-Many merupakan relasi yang menunjukkan hubungan antar tabel dimana baris pada tabel induk dapat terhubung dengan satu atau lebih baris di tabel anak. Sementara baris pada tabel anak hanya dapat terhubung dengan satu baris di tabel induk.
4. Many-to-Many merupakan relasi yang menunjukkan hubungan antar tabel dimana baris pada tabel induk dapat terhubung dengan satu atau lebih baris di tabel anak. Berlaku sebaliknya pada tabel anak yang dapat terhubung dengan satu atau lebih baris di tabel induk.
5. Junction Table merupakan tabel yang digunakan untuk mengatur kombinasi baris pada relasi many-to-many. Junction table berisikan foreign key dari kedua tabel yang memiliki relasi many-to-many.
   
##

### Langkah Percobaan Praktikum ###

### A. Model ###

1. Memastikan telah terdapatnya table users dengan kolom id, createdAt, updatedAt, name, email, dan password, yang dibuat menggunakan migration pada percobaan praktikum sebelumnya. Terlihat pada gambar bahwa informasi seluruh kolom pada table users telah tersedia

<img width="849" alt="Screenshot 2023-11-08 124236" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/16bf09a8-4d19-4d1e-b166-fe134d2d732e">

---

2. Membersihkan isi File User.php yang ada sebelumnya, kemudian menuliskan sintaks baru seperti pada gambar
   
<img width="850" alt="Screenshot 2023-11-08 124251" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/be9bdc10-fb20-4eda-83e0-77e996c5a56a">

---

### B. Controller ###

1. Membuat File Controller baru bernamakan “HomeController.php” dalam folder app/Http/Controllers dengan melakukan copy dari File “ExampleController.php”. Proses selanjutnya dilakukan dengan menambahkan fungsi index()

<img width="791" alt="Screenshot 2023-11-08 124320" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f8e6a919-34c4-46ca-88c7-213fd2f1c605">

---

2. Menambahkan sintaks, yaitu baris 20 sesuai dengan modul praktikum, pada file routes/web.php
   
<img width="793" alt="Screenshot 2023-11-08 124333" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/286c4bfd-89d1-4b8b-ac55-67a1c7ae3c45">

---

3. Menjalankan aplikasi dengan memasukkan URL “localhost:8000”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “Hello, from lumen”
   
<img width="791" alt="Screenshot 2023-11-08 124352" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f3e4374b-6765-4d92-bf74-76b69ac82047">

---

### C. Request Handler ###

1. Menambahkan sintaks pada baris 5 sesuai dengan modul praktikum untuk melakukan import library request

<img width="794" alt="Screenshot 2023-11-08 124407" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/24f238ec-91d9-4946-9ce8-dfc5e9c29dfd">

---

2. Melakukan perubahan fungsi index pada baris 20-23 sesuai dengan modul praktikum
   
<img width="692" alt="Screenshot 2023-11-08 124428" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/78ac5038-0752-48d9-9115-46743d0c4032">

---

3. Menjalankan aplikasi dengan memasukkan URL “localhost:8000”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “Hello, from lumen! We got your request from endpoint: /”
   
<img width="584" alt="Screenshot 2023-11-08 124450" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4c1ba1ab-308a-4eaf-9ac4-75a33cff9066">

---

### D. Response Handler ###

1. Menambahkan sintaks pada baris 8 sesuai dengan modul praktikum untuk melakukan import library response
   
<img width="880" alt="Screenshot 2023-11-08 124505" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/70789dec-f293-4dfb-a105-0cf3860bb264">

---

2. Menambahkan sintaks pada baris 31 - 38 untuk membuat fungsi hello()

<img width="906" alt="Screenshot 2023-11-08 124523" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a35fd572-402a-4632-bea0-c0d20037035f">

---

3. Menambahkan sintaks pada baris 85 untuk menambahkan route /hello pada file routes/web.php

<img width="908" alt="Screenshot 2023-11-08 124538" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f16854dd-888e-4b88-a831-94044edf6730">

---

4. Menjalankan aplikasi dengan memasukkan URL “localhost:8000/hello”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “status” : “Success” dan “message” : “Hello, from lumen!”
   
<img width="572" alt="Screenshot 2023-11-08 124559" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/03afd55c-fc17-4e8a-886b-fddf95cdcd98">

---

### E. Penerapan ###

1. Menambahkan sintaks pada baris 5 sesuai dengan modul praktikum untuk melakukan import model user
   
<img width="823" alt="Screenshot 2023-11-08 124613" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/af2a2063-6e43-40b5-9a60-f443d1f2dbbb">

---

2. Menambahkan sintaks pada baris 43 - 93 untuk menambahkan function defaultUser(), createUser(), dan getUsers() pada HomeController.php
   
<img width="806" alt="Screenshot 2023-11-08 124628" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/461d9c5d-daf9-405e-880d-eac213c55500">

<img width="787" alt="Screenshot 2023-11-26 010709" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/882d1bc7-12f6-467a-b1e8-ba63de1e57da">

<img width="788" alt="Screenshot 2023-11-26 010807" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/17a47f3a-5020-42d9-97e8-aabd866724ef">

---

3. Menambahkan sintaks pada baris 87 - 91 untuk menambahkan ketiga route pada file routes/web.php menggunakan group route

<img width="950" alt="Screenshot 2023-11-08 124645" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d05a857c-48e8-4a25-87a6-5b6f4a5f0083">

---

4. Menjalankan aplikasi pada route /users/default menggunakan postman (URL “http://localhost:8000/users/default” dan method “POST”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (Success), message (Default user created), dan data user (name “Nahida”, email “nahida@akademiya.ac.id”, password “smol”, updated_at, created_at, dan id “1”)

<img width="650" alt="Screenshot 2023-11-08 124708" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/06a3b282-a355-4d5d-a151-e6a05cc26cc7">

---

5. Menjalankan aplikasi pada route /users/new menggunakan postman (URL “http://localhost:8000/users/new”, method “POST”, dan body (name “Cyno”, email “cyno@akademiya.ac.id”, password “mahamatra”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (Success), message (New user created), dan data user (name “Cyno”, email “cyno@akademiya.ac.id”, password “mahamatra”, updated_at, created_at, dan id “3”)

<img width="659" alt="Screenshot 2023-11-08 124727" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/71e43997-b776-4e23-bcb1-827d9563e9a6">

---

6. Menjalankan aplikasi pada route /users/all menggunakan postman (URL “http://localhost:8000/users/all” dan method “GET”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (Success), message (all users grabbed), data user 1 (id “1”, created_at, updated_at, name “Nahida”, email “nahida@akademiya.ac.id”, dan password “smol”), dan data user 2 (id “2”, created_at, updated_at, name “Cyno”, email “cyno@akademiya.ac.id”, dan password “mahamatra”

<img width="651" alt="Screenshot 2023-11-08 124744" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/18942a09-b2f5-4754-85ad-6a7c7823a9b4">

---

### Kesimpulan Praktikum ###

1. Model:
- Model bertanggung jawab untuk menyiapkan, mengatur, dan memanipulasi data dalam database.
- Pembuatan model pada Lumen dilakukan secara manual disebabkan terdapatnya keterbatasan perintah "Artisan".
- Contoh implementasi Model : User dengan atribut yang sesuai.
  
2. Controller:
- Controller berfungsi sebagai tempat berkumpulnya logika pemrograman yang memisahkan organisasi data pada database.
- Contoh implementasi Controller : Pembuatan salinan controller dengan fungsi index() .

3. Request Handler:
- Mahasiswa diajak untuk mengenal konsep request handler, yaitu fungsi yang berinteraksi dengan data yang dikirim oleh pengguna melalui request.
- Contoh implementasi Request Handler : Fungsi index() untuk menanggapi request.
  
4. Response Handler:
- Response handler bersifat sebagai fungsi untuk membentuk output yang diharapkan kepada pengguna, termasuk status code dan header.
- Contoh implementasi Response Handler : Fungsi hello() dengan memberikan respons JSON dan mengatur status code.
  
5. Implementasi CRUD:
- Melakukan import model User dan menambahkan tiga fungsi pada controller untuk melakukan operasi CRUD pada tabel users.
- Melakukan pembuatan route untuk setiap fungsi CRUD menggunakan group route.
   
##


<img width="767" alt="Screenshot 2023-11-08 124928" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7600b31c-f62e-45c7-84d6-b52d7bbb0ea7">
<img width="711" alt="Screenshot 2023-11-08 124946" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/703af407-cc2b-437c-9a1b-8f2ec9641072">
<img width="949" alt="Screenshot 2023-11-08 125005" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0d09dc0f-c15b-4b0f-b2af-4029f25821e5">
<img width="938" alt="Screenshot 2023-11-08 125024" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7d918c69-5f8f-4a27-aca2-5943164e6733">
<img width="939" alt="Screenshot 2023-11-08 125038" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/45799ed7-4830-4715-bf84-562f6da90c87">
<img width="954" alt="Screenshot 2023-11-08 125059" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9120bd33-cad8-426f-8836-b0da0c237817">
<img width="955" alt="Screenshot 2023-11-08 125114" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6da39f07-168d-4c6d-a5e6-140e15a741c9">
<img width="954" alt="Screenshot 2023-11-08 125128" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f388184-77cb-4716-bc5a-6f8ad9fecbbb">
<img width="953" alt="Screenshot 2023-11-08 125144" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/77287ffb-8d29-4fde-ae12-6c1d9e0f1151">
<img width="884" alt="Screenshot 2023-11-08 125206" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ad14d367-c0a7-4165-97a4-38764110cba6">
<img width="885" alt="Screenshot 2023-11-08 125222" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/fb4f99e9-2254-44e4-90f2-8ef979fb1bb7">
<img width="886" alt="Screenshot 2023-11-08 125237" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/33f900fc-b62b-4c6d-95b6-424b794bd71e">
<img width="886" alt="Screenshot 2023-11-08 125256" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/361cd3af-1154-4bed-b9c3-13b4549c1f31">
<img width="884" alt="Screenshot 2023-11-08 125317" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f8a53a4-8061-4bf2-b3fb-8137d01e0d2f">
<img width="887" alt="Screenshot 2023-11-08 125332" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0c4aaf3c-6322-4419-b5e3-bf786fa8f6f8">
<img width="886" alt="Screenshot 2023-11-08 125350" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/edae2ab7-ed39-4f1c-9df6-e6b5a9a7c7f8">
<img width="937" alt="Screenshot 2023-11-08 125407" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/023fe14e-7d0e-4e5c-8d0c-e54b49f53a93">
