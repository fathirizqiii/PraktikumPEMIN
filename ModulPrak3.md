Melakukan penginstalan NodeJS sebagai langkah awal dalam mengerjakan praktikum

<img width="494" alt="Screenshot 2023-11-08 111751" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b1ce0663-6961-4a24-a86a-aba8f5613ac0">

---
   
Menjalankan perintah “node -v” untuk melakukan pemeriksaan apakah NodeJS sudah terinstall

<img width="535" alt="Screenshot 2023-11-08 111810" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e0a0ffd6-30ee-4a1c-bec3-71f19402dc65">

---
   
Masuk ke dalam direktori C:\Users\Lenovo\Downloads\PEMIN\Praktikum PEMIN\express-mongodb, kemudian jalankan perintah “npm init -y” untuk menggenerate file package.json

<img width="826" alt="Screenshot 2023-11-08 111835" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4424288c-829f-4e3a-8905-5bf04dc717a3">

---
   
Menjalankan perintah “npm i express mongoose dotenv” untuk menginstall express, mongoose, dan dotenv

<img width="826" alt="Screenshot 2023-11-08 111848" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/527fd06a-0884-4f48-9593-2277db604737">

---
   
Membuat file index.js pada root folder, kemudian masukkan kode sesuai dengan langkah praktikum. Setelah itu, coba jalankan aplikasi dengan perintah “node index.js”. Sesuai pada output di atas, terlihat bahwa proses hanya stuck pada “Running on port 8000” tanpa membuat koneksi yang sukses (Mongo Connected)

<img width="727" alt="Screenshot 2023-11-08 111905" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a39d491a-9738-491c-9c79-08cdc0e0fdca">

---

Melakukan pembuatan file .env dengan menambahkan “PORT = 5000”

<img width="479" alt="Screenshot 2023-11-08 111927" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/39d26c72-6439-48ea-8b87-36a5f2cc38b6">

---

Melakukan pengubahan kode pada listening port sesuai dengan langkah praktikum

<img width="839" alt="Screenshot 2023-11-08 111948" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a389337f-0d21-432f-82b5-d1da88736990">

---

Memasukkan connection string yang terdapat pada compas atau atlas, yaitu mongodb://localhost:27017

<img width="424" alt="Screenshot 2023-11-08 112007" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/850bf2bc-e3ac-49ec-9e3d-d03aad8c4947">

---

Menambahkan baris kode baru pada file index.js, kemudian jalankan aplikasi kembali dengan perintah “node index.js”. Terlihat pada output di atas bahwa Mongo telah terkoneksi (Mongo Connected)

<img width="565" alt="Screenshot 2023-11-08 112023" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1be91f29-a52b-442c-a83c-ca7720edef5c">

---

Melakukan pengecekan pada web browser apakah Koneksi Mongo telah sukses dengan memasukkan URL localhost:5000. Sesuai pada gambar, koneksi telah berjalan sukses dengan mengembalikan output message berupa nama dan nim.

<img width="477" alt="Screenshot 2023-11-08 112049" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/81a03467-ed33-49d3-a019-346c21992243">

---

Membuat direktori routes di tingkat yang sama dengan index.js, kemudian membuat file book.route.js di dalamnya

<img width="600" alt="Screenshot 2023-11-08 112106" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/691ee9a2-e48e-4b15-aca6-784500aa74a6">

---

Menambahkan sintaks terkait fungsi getOneBook, createBook, updateBook, dan deleteBook

<img width="602" alt="Screenshot 2023-11-08 112122" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b514e801-98f8-4cc2-88fd-e6a47ee88af4">

---

Menambahkan dua baris sintaks, yaitu “const bookRoutes” dan “app.use(‘/books’, bookRoutes)” untuk melakukan proses import book.route.js di dalam file index.js

<img width="647" alt="Screenshot 2023-11-08 112140" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/70d8ded3-a6a0-463a-a65a-e3ac8b62da16">

---

Melakukan pengujian endpoint POST menggunakan Postman. Terlihat pada gambar di atas bahwa output yang dihasilkan telah sesuai dengan input endpoint POST

<img width="629" alt="Screenshot 2023-11-08 112213" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f150a7c-62e1-4b06-8bff-74dfb95c9d6a">

---
    
Membuat direktori controllers di tingkat yang sama dengan index.js, kemudian membuat file book.controller.js di dalamnya. Setelah itu, tambahkan sintaks terkait fungsi getOneBook, createBook, updateBook, dan deleteBook

<img width="689" alt="Screenshot 2023-11-08 112251" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/397d59bb-17c5-49d7-90bd-bbcb845181b9">

---

Melakukan import book.controller.js di dalam file book.route.js

<img width="834" alt="Screenshot 2023-11-08 112310" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/931f6a39-96c6-4db0-8ae3-4078423b5a0e">

---

Melakukan modifikasi fungsi agar dapat memanggil fungsi dari book.controller.js

<img width="820" alt="Screenshot 2023-11-08 112327" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7fa6a680-6766-47e4-b693-c8ceea7a28ba">

---

Melakukan pengujian kembali pada endpoint post menggunakan Postman. Terlihat pada gambar di atas bahwa output yang dihasilkan sesuai dengan percobaan endpoint post sebelumnya

<img width="646" alt="Screenshot 2023-11-08 112355" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9c82a12d-0172-41e6-a36d-40400842f0f8">

---

Membuat direktori models di tingkat yang sama dengan index.js, kemudian membuat file book.model.js di dalamnya. Setelah itu, tambahkan baris kode sesuai dengan langkah praktikum

<img width="571" alt="Screenshot 2023-11-08 112416" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/aa868504-2a92-43f3-963b-5d0175495436">

---

Menghapus semua data, yaitu collection books, melalui aplikasi MongoDB Compass

<img width="760" alt="Screenshot 2023-11-08 112431" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ed484acf-ccbf-476b-8cb6-8904b0995c63">

---

Melakukan import book.model.js pada file book.controller.js

<img width="831" alt="Screenshot 2023-11-08 112445" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6fa40fd6-d203-4111-ac5c-cb0b316e4c26">

---
    
Melakukan perubahan pada fungsi createBook seperti sintaks di atas

<img width="676" alt="Screenshot 2023-11-08 112512" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/de72511e-5c49-42f6-8ca0-56b17ba33afd">

---

Membuat dua buah buku, bernamakan “Dilan 1990” dan “Dilan 1991” dengan data sesuai dengan langkah praktikum yang ada, menggunakan endpoint POST pada Postman

<img width="656" alt="Screenshot 2023-11-08 112544" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ce6b5a80-147a-4e47-8b97-f470e7ad4338">

---

Melakukan proses perubahan terhadap fungsi getAllBooks dan getOneBook sesuai dengan sintaks pada langkah praktikum

<img width="674" alt="Screenshot 2023-11-08 112713" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a6aaf33c-b928-4a4a-90a0-06dcf42f0fc8">

<img width="791" alt="Screenshot 2023-11-08 112734" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/edf4abd2-645c-43f6-be3c-ccb4a6f75654">

---

Menampilkan semua buku yang ada dan Buku “Dilan 1990” (Parameter ID) dengan menggunakan endpoint GET pada Postman.

<img width="656" alt="Screenshot 2023-11-08 112818" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/94d48c35-8f56-49b0-bf21-2cafb8ce6814">

---

Melakukan proses perubahan pada fungsi updateBook sesuai dengan sintaks langkah praktikum

<img width="767" alt="Screenshot 2023-11-08 121546" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f48e836a-7256-4a30-96c4-c860d73f90eb">

---

Mengubah Title pada Buku “Dilan 1991” menjadi “Fathi 1991” menggunakan endpoint PUT pada Postman. Operasi update ini menggunakan parameter ID dari Buku “Dilan 1991”

<img width="674" alt="Screenshot 2023-11-08 112713" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/613725fa-d31f-40de-8bbb-28fa4696a347">

---

Melakukan proses perubahan pada fungsi deleteBook sesuai dengan sintaks langkah praktikum

<img width="791" alt="Screenshot 2023-11-08 112734" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/8afb2763-4c3a-4ccb-9113-ace765c452e0">

---

Menghapus Buku “Dilan 1990” dengan menggunakan parameter ID buku tersebut pada Postman. Terlihat pada gambar bahwa berhasil “menghapus satu buku”.

<img width="685" alt="Screenshot 2023-11-08 112758" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1a94068b-cdb4-4a8a-88fe-062c8ebf1a9a">

---

Menampilkan keseluruhan data Buku dengan endpoint GET pada Postman untuk mengecek hasil akhir dari percobaan sebelumnya. Terlihat pada gambar di atas bahwa jumlah buku hanya tersisa 1 (Buku “Dilan 1990” sudah sukses terhapus) dan Buku “Dilan 1991” telah berubah menjadi “Fathi 1991”

<img width="656" alt="Screenshot 2023-11-08 112818" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/256d3626-f572-4b93-9eae-92fac3d97cb4">

]()


