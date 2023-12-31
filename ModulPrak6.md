# Praktikum 6 : Model, Controller dan Request-Response Handler

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Mengimplementasikan model
2. Mengimplementasikan controller
3. Mengimplementasikan request handler
4. Mengimplementasikan response handler

##

### Dasar Teori Praktikum ###
1. Model merupakan bagian yang bertugas untuk menyiapkan, mengatur, memanipulasi, dan mengorganisasikan data yang ada di database. Model merepresentasikan kolom apa saja yang ada pada database, termasuk relasi dan primary key.
2. Controller merupakan bagian yang menjadi tempat berkumpulnya logika pemrograman yang digunakan untuk memisahkan organisasi data pada database. Dalam beberapa kasus, controller menjadi penghubung antara model dan view pada arsitektur MVC
3. Request handler merupakan fungsi yang digunakan untuk berinteraksi dengan request yang datang. Request handler dapat digunakan untuk melihat apa saja yang dikirimkan oleh user seperti parameter, query, dan body.
4. Response handler merupakan fungsi yang digunakan untuk membentuk output yang diharapkan kepada user dan beberapa properti selain data, seperti status code dan header.
   
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
- Contoh implementasi Controller : Pembuatan salinan controller dengan fungsi "index()" .

3. Request Handler:
- Mahasiswa diajak untuk mengenal konsep request handler, yaitu fungsi yang berinteraksi dengan data yang dikirim oleh pengguna melalui request.
- Contoh implementasi Request Handler : Fungsi "index()" untuk menanggapi request.
  
4. Response Handler:
- Response handler bersifat sebagai fungsi untuk membentuk output yang diharapkan kepada pengguna, termasuk status code dan header.
- Contoh implementasi Response Handler : Fungsi "hello()" dengan memberikan respons JSON dan mengatur status code.
  
5. Implementasi CRUD:
- Melakukan import model "User" dan menambahkan tiga fungsi pada controller untuk melakukan operasi CRUD pada tabel "users".
- Melakukan pembuatan route untuk setiap fungsi CRUD menggunakan group route.
   
##
