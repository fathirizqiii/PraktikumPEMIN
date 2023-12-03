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
3. One-to-Many merupakan relasi yang menunjukkan hubungan antar tabel dimana baris pada tabel induk dapat terhubung dengan satu atau lebih baris di tabel anak. Di lain sisi, baris pada tabel anak hanya dapat terhubung dengan satu baris di tabel induk.
4. Many-to-Many merupakan relasi yang menunjukkan hubungan antar tabel dimana baris pada tabel induk dapat terhubung dengan satu atau lebih baris di tabel anak. Berlaku sebaliknya pada tabel anak, yaitu dapat terhubung dengan satu atau lebih baris di tabel induk.
5. Junction Table merupakan tabel yang digunakan untuk mengatur kombinasi baris pada relasi many-to-many. Junction table berisikan foreign key dari kedua tabel yang memiliki relasi many-to-many.
   
##

### Langkah Percobaan Praktikum ###

### A. Pembuatan Tabel ###

1. Memastikan database bernamakan “lumenpost” telah terbuat dan server database telah aktif sebagai langkah awal dalam membuat migrasi database ataupun membuat table
   
<img width="767" alt="Screenshot 2023-11-08 124928" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7600b31c-f62e-45c7-84d6-b52d7bbb0ea7">

---
2. Melakukan pengubahan konfigurasi database pada file .env dengan mengganti DB_DATABASE menjadi “lumenpost” sesuai pada gambar
   
<img width="711" alt="Screenshot 2023-11-08 124946" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/703af407-cc2b-437c-9a1b-8f2ec9641072">

---

3. Mengubah 2 baris sintaks pada file app.php dalam folder bootstrap (menghapus “//” pada baris 26 dan 27) untuk menghidupkan beberapa library bawaan dari lumen
<img width="949" alt="Screenshot 2023-11-08 125005" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0d09dc0f-c15b-4b0f-b2af-4029f25821e5">

---

4. Menjalankan 4 perintah sesuai dengan modul praktikum untuk membuat file migration (create_posts_table, create_comments_table, create_tags_table, dan create_post_tag_table)

<img width="938" alt="Screenshot 2023-11-08 125024" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7d918c69-5f8f-4a27-aca2-5943164e6733">

--- 

5. Melakukan pengubahan fungsi up() pada file migrasi create_posts_table, yaitu menambahkan baris 17 seperti pada gambar

<img width="939" alt="Screenshot 2023-11-08 125038" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/45799ed7-4830-4715-bf84-562f6da90c87">

---

6. Melakukan pengubahan fungsi up() pada file create_comments_table, yaitu menambahkan baris 17 dan 18 seperti pada gambar
   
<img width="954" alt="Screenshot 2023-11-08 125059" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9120bd33-cad8-426f-8836-b0da0c237817">

---

7. Melakukan pengubahan fungsi up() pada file create_tags_table, yaitu menambahkan baris 17 seperti pada gambar
   
<img width="955" alt="Screenshot 2023-11-08 125114" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6da39f07-168d-4c6d-a5e6-140e15a741c9">

---

8. Melakukan pengubahan fungsi up() pada file create_post_tag_table, yaitu menambahkan baris 17 dan 18 seperti pada gambar
   
<img width="954" alt="Screenshot 2023-11-08 125128" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f388184-77cb-4716-bc5a-6f8ad9fecbbb">

---

9. Menjalankan perintah “php artisan migrate” untuk melakukan migrasi database. Terlihat pada gambar bahwa proses yang dijalankan berhasil
    
<img width="953" alt="Screenshot 2023-11-08 125144" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/77287ffb-8d29-4fde-ae12-6c1d9e0f1151">

---

### B. Pembuatan Model ###

1. Membuat file bernamakan Post.php dalam folder app/Models, kemudian menambahkan sintaks sesuai dengan modul praktikum
   
<img width="884" alt="Screenshot 2023-11-08 125206" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/ad14d367-c0a7-4165-97a4-38764110cba6">

---

2. Membuat file bernamakan Comment.php dalam folder app/Models, kemudian menambahkan sintaks sesuai dengan modul praktikum
   
<img width="885" alt="Screenshot 2023-11-08 125222" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/fb4f99e9-2254-44e4-90f2-8ef979fb1bb7">

---

3. Membuat file bernamakan Tag.php dalam folder app/Models, kemudian menambahkan sintaks sesuai dengan modul praktikum
   
<img width="886" alt="Screenshot 2023-11-08 125237" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/33f900fc-b62b-4c6d-95b6-424b794bd71e">

---

### C. Relasi One-to-Many ###

1. Menambahkan sintaks pada baris 27 - 31 untuk menambahkan fungsi comments() pada file Post.php
   
<img width="886" alt="Screenshot 2023-11-08 125256" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/361cd3af-1154-4bed-b9c3-13b4549c1f31">

---

2. Menambahkan sintaks pada baris 27 - 31 untuk menambahkan fungsi post() dan atribut postId pada $fillable pada file Comment.php
   
<img width="884" alt="Screenshot 2023-11-08 125317" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9f8a53a4-8061-4bf2-b3fb-8137d01e0d2f">

---

3. Membuat File PostController.php dalam folder app/Http/Controllers, kemudian mengisikan sintaks sesuai dengan modul praktikum
    
<img width="887" alt="Screenshot 2023-11-08 125332" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0c4aaf3c-6322-4419-b5e3-bf786fa8f6f8">

---

4. Membuat File CommentController.php dalam folder app/Http/Controllers, kemudian mengisikan sintaks sesuai dengan modul praktikum
   
<img width="886" alt="Screenshot 2023-11-08 125350" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/edae2ab7-ed39-4f1c-9df6-e6b5a9a7c7f8">

---

5. Menambahkan sintaks pada baris 93 - 100 sesuai dengan modul praktikum pada file web.php dalam folder routes
   
<img width="937" alt="Screenshot 2023-11-08 125407" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/023fe14e-7d0e-4e5c-8d0c-e54b49f53a93">

---

6. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts”, method “POST”, dan content “disana engkau berdua”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“New post created”), dan data post (content “disana engkau berdua”, updated_at, created_at, id “1”)
   
<img width="653" alt="Screenshot 2023-12-03 055140" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/339885da-117f-4d17-b7fe-5fddcb1ab1c7">

---

7. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/comments”, method “POST”, dan body (review “disini aku yang sendiri”, postId “1”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“New comment created”), dan data comment (review “disini aku yang sendiri”, updated_at, created_at, id “1”)
   
<img width="671" alt="Screenshot 2023-12-03 055213" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0973a125-6a97-4f13-8db1-53e92f520565">

---

8. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/1” dan method “GET”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“All post grabbed”), dan data post (id “1”, content “disana engkau berdua”, comments (id “1”, created_at, updated_at, review “disini aku yang sendiri”, postId “1”))
   
<img width="674" alt="Screenshot 2023-12-03 055241" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d6a8176d-6b55-459c-af76-ddd3eb48f58a">

---

### D. Relasi Many-to-Many ###

1. Menambahkan sintaks pada baris 37-41 untuk menambahkan fungsi tags() pada file Post.php
   
<img width="841" alt="Screenshot 2023-12-03 055301" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/2c8ed2ff-24bd-42ff-837e-22bb3f45971c">

---

2. Menambahkan sintaks pada baris 32-36 untuk menambahkan fungsi posts() pada file Tag.php
   
<img width="841" alt="Screenshot 2023-12-03 055316" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5fbbb6c6-d74a-4d3e-8319-8141e417c5a0">

---

3. Membuat File TagController.php dalam folder app/Http/Controllers, kemudian mengisikan sintaks sesuai dengan modul praktikum
   
<img width="731" alt="Screenshot 2023-12-03 055338" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6666c25a-5b01-40ac-b68f-e6634b099bc3">

---

4. Menambahkan sintaks pada baris 44 dan 50-59 untuk menambahkan fungsi addTag dan response tags pada PostController.php

<img width="602" alt="Screenshot 2023-12-03 055403" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b029ede8-b3bf-47e8-b03f-b2d0a7969518">

---

5. Menambahkan sintaks pada baris 97 dan 104-106 pada file web.php dalam folder routes

<img width="916" alt="Screenshot 2023-12-03 055420" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1a6f2445-882d-4ba5-9beb-6532dab081f6">

---

6. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/tags”, method “POST”, dan body (“name” : “jadul”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“New tag created”), dan data tag (name “jadul”, updated_at, created_at, dan id “1”)

<img width="661" alt="Screenshot 2023-12-03 055447" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/bae4ab1f-a684-4fad-8d3f-3062cda3b9c7">

---

7. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/1/tag/1” dan method “PUT”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true) dan message (“Tag added to post”)
   
<img width="662" alt="Screenshot 2023-12-03 055519" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/90ce0d05-1278-4283-a434-a78834c1619a">

---

8. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/1/” dan method “GET”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“All post grabbed”), dan data post (id “1”, content “disana engkau berdua”, comments (
(id “1”, created_at, updated_at, review “disini aku yang sendiri”, postId “1”), tags (id “1”, created_at, updated_at, name “jadul”, pivot)))

<img width="659" alt="Screenshot 2023-12-03 055542" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9250ac41-ff10-4066-87d1-267deda563c0">

---

9. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts”, method “POST”, dan body (“content” : “tanpamu apa artinya”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“New post created”), dan data post (content “tanpamu apa artinya”, updated_at, created_at, id “2”)
    
<img width="652" alt="Screenshot 2023-12-03 055729" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e7768345-500d-4e2e-8db5-b2bcaaf1d07c">

---

10. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/2/tag/1” dan method “PUT”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true) dan message (“Tag added to post”)
    
<img width="652" alt="Screenshot 2023-12-03 055750" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/174ec604-f806-4f7c-8c68-c9be5d7c3939">

---

11. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/tags”, method “POST”, dan body (“name” : “lagu”). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true), message (“Tag added to post”), dan data tag (name “lagu”, updated_at, created_at, id “4”)
    
<img width="652" alt="Screenshot 2023-12-03 055811" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/23487a88-0455-4524-b527-eee2082c5338">

---

12. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/2/tag/4” dan method “PUT”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true) dan message (“Tag added to post”)
    
<img width="653" alt="Screenshot 2023-12-03 055831" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0aa32cfd-0b86-4000-9ef0-889927ffab30">

---

13. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/1” dan method “GET”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true) dan message (“All post grabbed”), dan data post (id “1’”, content “disana engkau berdua”, comments (id “1”, created_at, updated_at, review “disini aku yang sendiri”, postId “1”), tags (id “1”, created_at, updated_at, name “jadul”, pivot)))
    
<img width="652" alt="Screenshot 2023-12-03 055854" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/76b5fe1d-b266-4564-a828-c1057affb2ab">

---

14. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/posts/2” dan method “GET”. Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi success (true) dan message (All post grabbed), dan data post (id “2’”, content “tanpamu apa artinya”, comments, tags 1 (id “1”, created_at, updated_at, name “jadul”, pivot), tags 2 (id “4”, created_at, updated_at, name “lagu”, pivot)))
    
<img width="652" alt="Screenshot 2023-12-03 055913" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d10eb58f-925c-435b-9ec4-f0de88caac18">

---

### Kesimpulan Praktikum ###

1. Pembuatan Tabel:
- Menggunakan beberapa tabel praktikum ini, seperti "posts", "comments", "tags", dan "post_tag".
- Membuat file migrasi untuk masing-masing tabel menggunakan perintah "Artisan".

2. Pembuatan Model:
- Membuat beberapa models untuk masing-masing tabel, yaitu "Post", "Comment", dan "Tag") di dalam folder "app/Models".
- Dalam model "Post", fungsi "comments(): ditambahkan untuk menunjukkan relasi One-to-Many dengan model "Comment".
- Dalam model "Comment", fungsi "post()" dan penambahan atribut postId pada $fillable digunakan untuk menunjukkan relasi Many-to-One dengan model "Post".
- Dalam model "Post", fungsi "tags()" ditambahkan untuk menunjukkan relasi Many-to-Many dengan model "Tag".
- Dalam model "Tag", fungsi "posts(): ditambahkan untuk menunjukkan relasi Many-to-Many dengan model "Post".

3. Pembuatan Controller:
- Membuat beberapa controllers, yaitu "PostController", "CommentController", dan "TagController",  untuk mengelola operasi CRUD (Create, Read, Update, dan Delete).
- Menambahkan beberapa fungsi, seperti "createPost()", "getPostById()", "createComment()", "createTag()", "addTag()", dan sebagainya, sesuai dengan kebutuhan.

4. Routes:
- Mengatur routes untuk masing-masing endpoint di dalam file "routes/web.php".
- Contoh endpoint yang ditambahkan : "/posts", "/posts/{id}", "/comments", "/tags", dan lainnya.

5. Penggunaan Postman:
- Percobaan dilakukan dengan menggunakan Postman untuk membuat postingan, menambahkan komentar, menambahkan tag, dan menampilkan hasilnya.
   
##
