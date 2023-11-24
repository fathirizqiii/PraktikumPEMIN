# Praktikum 4 : Basic Routing dan Migration

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Melakukan basic routing.
2. Mengakses routing
3. Melakukan migration ke database

##

### Langkah Percobaan Praktikum ###

### A. GET ###

1. Menambahkan sintaks sesuai dengan modul praktikum sebagai endpoint pada file web.php, yang berada di dalam folder routes, menggunakan method GET

<img width="768" alt="Screenshot 2023-11-08 122500" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/08a0b44d-759b-4299-bc0a-3f8f75031c3c">

---

2. Menjalankan perintah “php -S localhost:8000 -t public” untuk dapat menjalankan aplikasi. Terlihat pada gambar bahwa koneksi ke http:/localhost:8000 telah berhasil
   
<img width="734" alt="Screenshot 2023-11-08 122531" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b1d3c9c4-3291-48c4-8eea-16dcc2540723">

---

3. Mengakses browser dengan url “http://localhost:8000/get” dengan BASE_URL “localhost:8000” dan PATH “/get” setelah aplikasi berhasil dijalankan. Terlihat pada gambar bahwa proses mengakses url berhasil dengan mengembalikan output “GET”
   
<img width="453" alt="Screenshot 2023-11-08 122601" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/064b4149-9ac7-45a0-bbfb-c7e388c884d9">

---

### B. POST, PUT, PATCH, DELETE, dan OPTIONS ###

1. Menambahkan method POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php sesuai dengan sintaks pada modul praktikum
   
<img width="626" alt="Screenshot 2023-11-08 122619" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1269a698-3506-4962-a7ac-0ede76fc7b99">

---

2. Melakukan penginstalan extensions pada VSCode, yaitu Thunder Client, dengan membuka panel extensions

<img width="835" alt="Screenshot 2023-11-08 122635" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/720da3c4-e092-437c-b99e-5282a24be6cf">

---

3. Melakukan pengecekan Thunder Client pada activity bar di sebelah kiri setelah berhasil melakukan penginstalan. Terlihat pada gambar bahwa Thunder Client telah terinstall dengan terdapatnya logo seperti petir pada activity bar

<img width="161" alt="Screenshot 2023-11-08 122714" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/830dfb73-b2c7-45fa-85d1-ce4a6e495ef0">

---

4. Melakukan pembuatan request dengan menekan “New Request” pada ekstensi Thunder Client. Kemudian, memasukkan method (GET) dan URL (https://www.thunderclient.io/welcome) yang dituju
   
<img width="560" alt="Screenshot 2023-11-08 122746" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/bb436d86-d8b6-4777-a3aa-ad97f6c6f044">

---

5. Melakukan pengaksesan URL default Thunder Client (https://www.thunderclient.io/welcome) dengan methodnya (GET). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi message, about, createdBy,  launched, features, dan sebagainya
   
<img width="855" alt="Screenshot 2023-11-08 122807" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/81f0c30d-4d5e-46ef-9bef-4c27d7ad2f55">

---

6. Melakukan pengaksesan URL baru, yaitu (https://google.com) dengan methodnya (GET). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi itemscope itemtype, lang, content, dan sebagainya
   
<img width="875" alt="Screenshot 2023-11-08 122825" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4e888b80-ae96-4a7e-9e0f-2260774d2137">

---

### C. Migrasi Database ###

1. Membuat database bernamakan “lumenapi” dan memastikan server database aktif sebagai langkah awal dalam melakukan migrasi database

<img width="824" alt="Screenshot 2023-11-08 122846" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/bf11c790-3079-4cc8-a32d-1f94b574fc45">

---

2. Melakukan pengubahan konfigurasi database pada file .env, yaitu DB_USERNAME (root) dan DB_PASSWORD (-)
   
<img width="574" alt="Screenshot 2023-11-08 122914" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/92ae9766-0aad-444a-820c-be1aa62a800d">

---

3. Mengubah 2 baris sintaks pada file app.php, yang berada dalam folder bootstrap, sesuai dengan modul praktikum (menghapus “//” pada 2 baris sintaks tersebut) untuk menghidupkan beberapa library bawaan Lumen
   
<img width="620" alt="Screenshot 2023-11-08 122933" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/21e3a18d-82ab-440f-94e7-5080cf659b2b">

---

4. Menjalankan perintah “php artisan make:migration create_users_table” dan “php artisan make:migration create_products_table” untuk membuat migrasi pada table users dan products. 

<img width="866" alt="Screenshot 2023-11-08 122952" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5b646b03-2b39-44f8-abc0-f828b2e3f1c4">

---

5. Mengubah fungsi up() pada file migrasi create_users_table yang baru terbuat setelah dijalankannya proses membuat migrasi untuk table users. Pada file migrasi, kita akan menemukan fungsi up(), yang akan digunakan saat user melakukan migrasi, dan fungsi down(), yang akan digunakan saat user ingin melakukan rollback migrasi
   
<img width="923" alt="Screenshot 2023-11-08 123037" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/96b70dab-b926-4701-b5ab-87f5b4916c72">

---

6. Mengubah fungsi up() pada file migrasi create_products_table yang baru terbuat setelah dijalankannya proses membuat migrasi untuk table products. Pada file migrasi, kita akan menemukan fungsi up(), yang akan digunakan saat user melakukan migrasi, dan fungsi down(), yang akan digunakan saat user ingin melakukan rollback migrasi
   
<img width="925" alt="Screenshot 2023-11-08 123052" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/7c6794d8-afb2-4d3a-9c78-2b5d6321f0d7">

---

7. Menjalankan perintah “php artisan migrate” untuk melakukan migrasi database
   
<img width="721" alt="Screenshot 2023-11-08 123110" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/569cfe91-5e9b-4733-a06d-55a3dfb2e14f">

---

### Kesimpulan Praktikum ###

1. Basic Routing:

Mahasiswa diminta untuk menambahkan endpoint dengan metode GET pada file web.php untuk menanggapi permintaan GET pada URL /get.
Dengan menjalankan server dan membuka browser ke http://localhost:8000/get, mahasiswa dapat menguji implementasi dasar routing.

2. Metode POST, PUT, PATCH, DELETE, dan OPTIONS:

Pada langkah ini, mahasiswa diminta untuk menambahkan rute untuk metode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php.
Penggunaan ekstensi Thunder Client pada VSCode memungkinkan mahasiswa untuk membuat permintaan ke server dengan metode yang sesuai.
Tujuan percobaan ini adalah memastikan server merespons dengan benar untuk setiap metode yang diimplementasikan.

3. Migrasi Database:

Mahasiswa diminta untuk mengkonfigurasi database di file .env dan menghidupkan fasilitas bawaan Lumen untuk menggunakan Eloquent.
Dengan membuat dua file migrasi untuk tabel "users" dan "products" menggunakan perintah php artisan make:migration, mahasiswa memahami proses pembuatan migrasi.
Melalui modifikasi struktur tabel dalam fungsi up() pada masing-masing file migrasi, mahasiswa memahami konsep pengaturan skema database.
Menjalankan migrasi dengan perintah php artisan migrate menghasilkan pembuatan tabel baru dalam database.

### 
