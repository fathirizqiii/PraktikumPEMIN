# Praktikum 3 : Integrasi MongoDB dan Express

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Memasang Node.JS dan inisiasi project Express
2. Memasang package Mongoose dan Dotenv
3. Menghubungkan project Express ke MongoDB
4. Membuat routing dan controller dengan Express
5. Membuat model skema untuk struktur data MongoDB
6. Melakukan operasi CRUD dengan Express

##

### Dasar Teori Praktikum ###

1. Express.js merupakan suatu framework web app untuk Node.js yang ditulis dengan bahasa pemrograman JavaScript. Framework open source ini dibuat oleh TJ Holowaychuk pada tahun 2010 lalu. Express.js ini merupakan framework back end, yang artinya bertanggung jawab dalam mengatur fungsionalitas website, seperti pengelolaan routing dan session, permintaan HTTP, penanganan error, serta pertukaran data di server.

2. Mongoose merupakan pustaka berbasis Node.js yang digunakan untuk melakukan pemodelan data pada MongoDB. Mongoose menyediakan feature, antara lain model data application berbasis schema, dan juga termasuk built-in type casting, validation, query building, business logic hooks, serta masih banyak lagi yang menjadi keandalan mongoose.

3. Async Await merupakan sebuah fungsi yang mengembalikan sebuah promise dan hanya berjalan di dalam Async. Await bertujuan untuk menunda jalannya Async hingga proses dari Await tersebut berhasil dieksekusi.

4. Model merupakan bagian yang bertugas untuk menyiapkan, mengatur, memanipulasi, dan mengorganisasikan data yang ada di database.

5. Controller merupakan bagian yang menjadi tempat berkumpulnya logika pemrograman yang digunakan untuk memisahkan organisasi data pada database. Dalam beberapa kasus, controller menjadi penghubung antara model dan view pada arsitektur MVC (Model, View, Controller)

6. Router berfungsi untuk mengatur pintu masuk yang berupa request pada aplikasi, dengan memilah dan mengolah request url untuk kemudian diproses sesuai dengan tujuan akhir url tersebut. Bisa jadi url tersebut berfungsi untuk mengambil data, kemudian menampilkannya, menghapus data, menampilkan form, sampai mengolah session.

##

### Langkah Percobaan Praktikum ###

### A. Percobaan instalasi NodeJS ###

1. Melakukan penginstalan NodeJS sebagai langkah awal dalam mengerjakan praktikum

<img width="494" alt="Screenshot 2023-11-08 111751" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b1ce0663-6961-4a24-a86a-aba8f5613ac0">

---
   
2. Menjalankan perintah “node -v” untuk melakukan pemeriksaan apakah NodeJS sudah terinstall

<img width="535" alt="Screenshot 2023-11-08 111810" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e0a0ffd6-30ee-4a1c-bec3-71f19402dc65">

---

### B. Inisiasi project Express dan pemasangan package ###
   
1. Masuk ke dalam direktori C:\Users\Lenovo\Downloads\PEMIN\Praktikum PEMIN\express-mongodb, kemudian jalankan perintah “npm init -y” untuk menggenerate file package.json

<img width="826" alt="Screenshot 2023-11-08 111835" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4424288c-829f-4e3a-8905-5bf04dc717a3">

---
   
2. Menjalankan perintah “npm i express mongoose dotenv” untuk menginstall express, mongoose, dan dotenv

<img width="826" alt="Screenshot 2023-11-08 111848" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/527fd06a-0884-4f48-9593-2277db604737">

---

### C. Koneksi Express ke MongoDB ###
   
1. Membuat file index.js pada root folder, kemudian masukkan kode sesuai dengan langkah praktikum. Setelah itu, coba jalankan aplikasi dengan perintah “node index.js”. Sesuai pada output di atas, terlihat bahwa proses hanya stuck pada “Running on port 8000” tanpa membuat koneksi yang sukses (Mongo Connected)

<img width="727" alt="Screenshot 2023-11-08 111905" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a39d491a-9738-491c-9c79-08cdc0e0fdca">

---

2. Melakukan pembuatan file .env dengan menambahkan “PORT = 5000”

<img width="479" alt="Screenshot 2023-11-08 111927" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/39d26c72-6439-48ea-8b87-36a5f2cc38b6">

---

3. Melakukan pengubahan kode pada listening port sesuai dengan langkah praktikum

<img width="839" alt="Screenshot 2023-11-08 111948" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a389337f-0d21-432f-82b5-d1da88736990">

---

4. Memasukkan connection string yang terdapat pada compas atau atlas, yaitu mongodb://localhost:27017

<img width="424" alt="Screenshot 2023-11-08 112007" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/850bf2bc-e3ac-49ec-9e3d-d03aad8c4947">

---

5. Menambahkan baris kode baru pada file index.js, kemudian jalankan aplikasi kembali dengan perintah “node index.js”. Terlihat pada output di atas bahwa Mongo telah terkoneksi (Mongo Connected)

<img width="565" alt="Screenshot 2023-11-08 112023" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1be91f29-a52b-442c-a83c-ca7720edef5c">

---

6. Melakukan pengecekan pada web browser apakah Koneksi Mongo telah sukses dengan memasukkan URL localhost:5000. Sesuai pada gambar, koneksi telah berjalan sukses dengan mengembalikan output message berupa nama dan nim.

<img width="477" alt="Screenshot 2023-11-08 112049" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/81a03467-ed33-49d3-a019-346c21992243">

---

### D. Pembuatan routing ###

1. Membuat direktori routes di tingkat yang sama dengan index.js, kemudian membuat file book.route.js di dalamnya

<img width="600" alt="Screenshot 2023-11-08 112106" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/691ee9a2-e48e-4b15-aca6-784500aa74a6">

---

2. Menambahkan sintaks terkait fungsi getOneBook, createBook, updateBook, dan deleteBook

<img width="602" alt="Screenshot 2023-11-08 112122" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b514e801-98f8-4cc2-88fd-e6a47ee88af4">

---

3. Menambahkan dua baris sintaks, yaitu “const bookRoutes” dan “app.use(‘/books’, bookRoutes)” untuk melakukan proses import book.route.js di dalam file index.js

<img width="647" alt="Screenshot 2023-11-08 112140" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/70d8ded3-a6a0-463a-a65a-e3ac8b62da16">

---

4. Melakukan pengujian endpoint POST menggunakan Postman. Terlihat pada gambar di atas bahwa output yang dihasilkan telah sesuai dengan input endpoint POST

<img width="629" alt="Screenshot 2023-11-08 112213" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f150a7c-62e1-4b06-8bff-74dfb95c9d6a">

---

### E. Pembuatan controller ###
    
1. Membuat direktori controllers di tingkat yang sama dengan index.js, kemudian membuat file book.controller.js di dalamnya. Setelah itu, tambahkan sintaks terkait fungsi getOneBook, createBook, updateBook, dan deleteBook

<img width="689" alt="Screenshot 2023-11-08 112251" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/397d59bb-17c5-49d7-90bd-bbcb845181b9">

---

2. Melakukan import book.controller.js di dalam file book.route.js

<img width="834" alt="Screenshot 2023-11-08 112310" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/931f6a39-96c6-4db0-8ae3-4078423b5a0e">

---

3. Melakukan modifikasi fungsi agar dapat memanggil fungsi dari book.controller.js

<img width="820" alt="Screenshot 2023-11-08 112327" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7fa6a680-6766-47e4-b693-c8ceea7a28ba">

---

4. Melakukan pengujian kembali pada endpoint post menggunakan Postman. Terlihat pada gambar di atas bahwa output yang dihasilkan sesuai dengan percobaan endpoint post sebelumnya

<img width="646" alt="Screenshot 2023-11-08 112355" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9c82a12d-0172-41e6-a36d-40400842f0f8">

---

### F. Pembuatan model ###

1. Membuat direktori models di tingkat yang sama dengan index.js, kemudian membuat file book.model.js di dalamnya. Setelah itu, tambahkan baris kode sesuai dengan langkah praktikum

<img width="571" alt="Screenshot 2023-11-08 112416" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/aa868504-2a92-43f3-963b-5d0175495436">

---

### G. Operasi CRUD ###

1. Menghapus semua data, yaitu collection books, melalui aplikasi MongoDB Compass

<img width="760" alt="Screenshot 2023-11-08 112431" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ed484acf-ccbf-476b-8cb6-8904b0995c63">

---

2. Melakukan import book.model.js pada file book.controller.js

<img width="831" alt="Screenshot 2023-11-08 112445" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6fa40fd6-d203-4111-ac5c-cb0b316e4c26">

---
    
3. Melakukan perubahan pada fungsi createBook seperti sintaks di atas

<img width="676" alt="Screenshot 2023-11-08 112512" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/de72511e-5c49-42f6-8ca0-56b17ba33afd">

---

4. Membuat dua buah buku, bernamakan “Dilan 1990” dan “Dilan 1991” dengan data sesuai dengan langkah praktikum yang ada, menggunakan endpoint POST pada Postman

<img width="656" alt="Screenshot 2023-11-08 112544" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ce6b5a80-147a-4e47-8b97-f470e7ad4338">
<img width="715" alt="Screenshot 2023-11-11 122713" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/63b75ee9-94cb-409d-8ff9-2916229e3a50">

---

5. Melakukan proses perubahan terhadap fungsi getAllBooks dan getOneBook sesuai dengan sintaks pada langkah praktikum

<img width="716" alt="Screenshot 2023-11-11 122744" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/827c23fb-ef57-413c-984e-7fe10e70eebc">

---

6. Menampilkan semua buku yang ada dan Buku “Dilan 1990” (Parameter ID) dengan menggunakan endpoint GET pada Postman.

<img width="716" alt="Screenshot 2023-11-11 122813" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/c7a05d5e-c7be-4c13-8ef9-8f46d3b3fe4f">

---

7. Melakukan proses perubahan pada fungsi updateBook sesuai dengan sintaks langkah praktikum

<img width="764" alt="Screenshot 2023-11-11 122916" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3e8d6a46-e69e-471b-a0a8-0d01739b74f8">

---

8. Mengubah Title pada Buku “Dilan 1991” menjadi “Fathi 1991” menggunakan endpoint PUT pada Postman. Operasi update ini menggunakan parameter ID dari Buku “Dilan 1991”
   
<img width="679" alt="Screenshot 2023-11-11 122957" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4f44749f-6955-415c-8019-9b3995cc050a">

---

9. Melakukan proses perubahan pada fungsi deleteBook sesuai dengan sintaks langkah praktikum
    
<img width="714" alt="Screenshot 2023-11-11 123019" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5cfa077d-4100-4e85-b164-01bd21e16536">

---

10. Menghapus Buku “Dilan 1990” dengan menggunakan parameter ID buku tersebut pada Postman. Terlihat pada gambar bahwa berhasil “menghapus satu buku”.

<img width="681" alt="Screenshot 2023-11-11 123134" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ac4d1c7d-bb04-410c-8cbe-7cbc6a660ebe">

---

11. Menampilkan keseluruhan data Buku dengan endpoint GET pada Postman untuk mengecek hasil akhir dari percobaan sebelumnya. Terlihat pada gambar di atas bahwa jumlah buku hanya tersisa 1 (Buku “Dilan 1990” sudah sukses terhapus) dan Buku “Dilan 1991” telah berubah menjadi “Fathi 1991”

<img width="673" alt="Screenshot 2023-11-11 123216" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a57eb28c-40a8-409d-92cb-0f46e47399ba">

---

### Kesimpulan ###


