# Praktikum 2 : CRUD MongoDB Compass dan Shell

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Melakukan operasi CRUD secara GUI dengan MongoDB Compass
2. Melakukan operasi CRUD secara CLI dengan MongoDB Shell

##

### Dasar Teori Praktikum ###
1. MongoDB Compass merupakan suatu tool berbasis Graphical User Interface (GUI) yang digunakan untuk berinteraksi dengan MongoDB yang terpasang secara on-premise dan MongoDB Atlas yang berbasis cloud. Tool ini dapat melakukan aktivitas/operasi dasar, seperti CREATE, READ, UPDATE, dan DELETE (CRUD) tanpa berhadapan dengan baris perintah (command line) MongoDB Shell

2. Di lain sisi, MongoDB Shell dapat melakukan operasi seperti MongoDB Compass, tetapi interaksi yang dilakukan MongoDB Shell ini berbasis Command Line Interface (CLI) sehingga diperlukan baris perintah untuk melakukan aktivitas/operasi dasar. MongoDB Shell dapat diakses langsung dari MongoDB Compass atau menggunakan mongosh pada Command Prompt

##

### Langkah Percobaan Praktikum ###

### A. MongoDB Compass ###

1. Melakukan koneksi ke MongoDB secara local (atlas), yaitu "mongodb://localhost:27017"
<img width="940" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5e1e493d-2f60-4fcd-b5b3-ffb7873b1d8c">

---

2. Membuat database yang bernamakan "bookstore" dengan collection bernama "books"
<img width="681" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3bfad5ff-d34e-41a4-8f5c-0dc46a6e6b70">

---

3. Melakukan insert buku pertama, yaitu "No Longer Human", dengan melakukan "Add Data" dan "Insert Document". Kemudian, isi data lain terkait buku ini, seperti author, year, pages, summary, dan publisher.
<img width="693" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/734c0ba0-b086-4fbc-82f6-5a9cbde7c5d0">

---

4. Melakukan insert buku kedua, yaitu "I Am a Cat" dengan mengisikan data, seperti author, year, pages, summary, dan publisher.
<img width="674" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/41a992a4-64db-4edb-93dd-d963298d6c86">

---

5. Melakukan pencarian buku dengan author bernamakan "Osamu Dazai" menggunakan parameter id buku. Setelah menekan button "find", buku yang memiliki atribut author "Ozamu Dazai" akan ditampilkan
<img width="743" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4ce8879f-6ed0-46da-b5ec-027b15781991">

---

6. Melakukan edit document dengan mengubah summary pada Buku "No Longer Human" menjadi "Buku yang bagus (Muhammad Fathi Rizqi, 215150707111016)
<img width="944" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d713bec1-e5aa-46ab-83b7-db028517e9d4">

---

7. Melakukan penghapusan (Remove Document) pada Buku "I Am a Cat"
<img width="762" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4a3bb339-5b33-4375-90a2-6afe5bd5ba3b">

---

### B. MongoDB Shell ###

1. Melakukan koneksi ke MongoDB Server dengan menggunakan command "mongosh" pada Command Prompt Windows
<img width="960" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a1d34b3c-fa47-4e8b-b36e-7f96c1da97e8">

---

2. Menjalankan perintah "show dbs" untuk melihat list database yang ada di server. Terlihat pada gambar bahwasannya database "bookstore" sudah ada karena telah ditambahkan pada langkah nomor 2
<img width="430" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ab726ea9-8903-49f8-aa4b-dec08374815e">

---

3. Menjalankan perintah "use bookstore" untuk berpindah ke database "bookstore". Terlihat pada gambar di bawah bahwasannya proses telah berhasil dilaksanakan
<img width="439" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/07cb3fcc-121c-4812-883e-3c74e2cdb9b9">

---

4. Menjalankan perintah "show collections" untuk melihat collections yang ada pada database. Terlihat pada output yang diberikan bahwa terdapat collection yang bernamakan "books"
<img width="654" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/89aa5c6f-e5bd-4fba-b43a-a1d064c6d985">

---

5. Menjalankan perintah "db.books.insertOne({title : "Overlord I", author : "Kugane Maruyama", ... }) untuk melakukan insert buku "Overlord 1" beserta elemen author, year, pages, summary, dan publisher
<img width="960" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/40d7f5f7-f3d9-48b2-b733-e4f385655fb9">

---

6. Menjalankan perintah "db.books.insertMany([{title : "The Setting Sun", author : "Osamu Dazai", ... }, {title : "Hujan", author : "Tere Liye", ... }]) untuk melakukan insert buku "The Setting Sun" dan "Hujan", beserta elemen author, year, pages, summary, dan publisher
<img width="946" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/34e02be5-c145-4de8-9f40-2ed685a41ace">

---

7. Menjalankan perintah "db.books.find()" untuk melakukan dan menampilkan pencarian semua buku. Seperti pada output di bawah, dapat dilihat bahwa terdapat buku "No Longer Human, Overlord I, The Setting Sun, dan Hujan"
<img width="596" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f4898df7-d579-4172-a171-c76f9b68d521">

---

8. Menjalankan perintah "db.books.find({author : "Osamu Dazai"})" untuk menampilkan seluruh buku dengan author bernamakan "Osamu Dazai". Terlihat pada output di bawah bahwasannya terdapat 2 buku dari author "Osamu Dazai" ini dengan elemen title, year, pages, summary, dan publisher yang berbeda.
<img width="584" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f1a43f7-ed8a-42b7-9827-1cc6824e819a">

---

9. Menjalankan perintah "db.books.updateOne({_id : Object Id(...)}, {$set : {summary : "Buku yang bagus (Muhammad Fathi Rizqi, 215150707111016}}) untuk melakukan perubahan summary pada buku "Hujan" menjadi "Buku yang bagus (Muhammad Fathi Rizqi, 215150707111016)
<img width="943" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9557f927-db55-44b1-bcea-4e624529c42f">

---

10. Menjalankan perintah "db.books.updateMany({author : "Osamu Dazai"}, {$set : {publisher : "Yen Press}}) untuk mengubah data publisher dari keseluruhan buku yang memiliki author "Osamu Dazai" menjadi "Yen Press"
<img width="773" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/19dd9531-1f58-4797-9252-fb811ebd2a5b">

---

11. Menjalankan perintah "db.books.deleteOne({_id : ObjectId(...)}) untuk melakukan penghapusan pada Buku "Overlord 1"
<img width="600" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b601e8e0-3bcc-4fde-a680-fc0a6b597d6b">

---

12. Menjalankan perintah "db.books.deleteMany({author : "Osamu Dazai"}) untuk melakukan penghapusan pada semua Buku "Osamu Dazai"
<img width="765" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/97c6d8f9-c72d-45eb-8183-22fd875b0a4c">

---

### Kesimpulan Praktikum ###
1. Praktikum ini bertujuan untuk membekali mahasiswa dengan keterampilan melakukan operasi CRUD pada MongoDB menggunakan dua pendekatan, yaitu MongoDB Compass dengan antarmuka grafis (GUI) dan MongoDB Shell melalui command line interface (CLI). 

2. MongoDB Compass dapat digunakan secara efisien untuk melakukan operasi CRUD tanpa perlu berhadapan dengan baris perintah, melibatkan langkah-langkah seperti koneksi ke MongoDB, membuat dan mengisi database, serta melakukan pencarian, pembaruan, dan penghapusan data.

3. MongoDB Shell dapat digunakan melalui CLI untuk melakukan operasi CRUD secara manual, termasuk koneksi ke MongoDB Server, navigasi dan manipulasi database dan collection, serta melakukan berbagai perintah seperti insert, find, update, dan delete.
##




















