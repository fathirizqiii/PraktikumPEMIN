# Praktikum 5 : Dynamic Route dan Middleware

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Melakukan dinamic routing.
2. Melakukan alias route.
3. Melakukan group route.
4. Melakukan Middleware

##

### Langkah Percobaan Praktikum ###

### A. Dynamic Route ###

1. Menambahkan sintaks pada baris 44 - 46 sesuai dengan modul praktikum untuk menambahkan dynamic routes pada aplikasi lumen
   
<img width="896" alt="Screenshot 2023-11-08 123439" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/1098de71-4ece-438f-af39-f7b320daef63">

---

2. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/user/1) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan User Id = 1
   
<img width="653" alt="Screenshot 2023-11-08 123502" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a5954201-978e-4d6a-9d7f-699fddfbaaf4">

---

3. Menambahkan sintaks pada baris 48 - 50 sesuai dengan modul praktikum untuk menambahkan parameter pada routes dengan tidak terbatas pada 1 variabel saja

<img width="879" alt="Screenshot 2023-11-08 123518" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/edbfbea2-56c6-446c-9d72-850735e2e2e3">

---

4. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/post/1/comments/2) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan Post ID = 1 dan Comments ID = 2
   
<img width="570" alt="Screenshot 2023-11-08 123547" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3da38874-fbbf-4bb5-926c-fc3e8f5e157a">

---

5. Menambahkan sintaks pada baris 52 - 54 sesuai dengan modul praktikum untuk menambahkan optional routes, yang tidak mengharuskan user untuk memberikan variabel pada endpointnya (user dibebaskan untuk menggunakan parameter variabel ataupun tidak ketika memanggil endpoint)

<img width="791" alt="Screenshot 2023-11-08 123606" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0604810d-2787-4dbd-800b-f1a5e06aca02">

---

6. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/users) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan data semua users

<img width="653" alt="Screenshot 2023-11-08 123635" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/2feb09d5-e19a-4100-abc1-d429510df468">

---

7. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/users/1) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan data user dengan id 1
   
<img width="657" alt="Screenshot 2023-11-08 123653" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b2f8db77-090f-484f-b3d4-65db3d83161a">

---

### B. Aliases Route ###

1. Menambahkan sintaks pada baris 56 - 64 sesuai dengan modul praktikum untuk menambahkan aliases route berupa login function (memberi nama pada route yang telah dibuat sehingga akan mempermudah proses pemanggilan route tersebut dalam aplikasi)

<img width="898" alt="Screenshot 2023-11-08 123709" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/c72a8461-d67b-442b-8baf-bec585cd5a32">

---

2. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/auth/login) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan “Hello User!”
   
<img width="644" alt="Screenshot 2023-11-08 123736" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9ac789c8-7bbd-45e1-be35-7afa6d01a552">

---

### C. Group Route ###

1. Menambahkan sintaks pada baris 66 - 70 sesuai dengan modul praktikum untuk menambahkan group route sehingga mempermudah proses penulisan route pada file web.php user

<img width="919" alt="Screenshot 2023-11-08 123752" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/2dc50573-690f-4fa6-b277-af7faa41028a">

---

### D. Middleware ###

1. Membuat File Middleware baru bernamakan “AgeMiddleware.php” dalam folder app/Http/Middleware dengan menyalin dari File “ExampleMiddleware”. Middleware sendiri berperan sebagai penengah antara komunikasi aplikasi dan client, yang berfungsi untuk membatasi siapa yang dapat berinteraksi dengan aplikasi dan semacamnya,

<img width="908" alt="Screenshot 2023-11-08 123808" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/8d3d95e3-46bf-4742-8dbb-0010fffe24bf">

---

2. Menambahkan sintaks (melakukan uncomment pada baris 78 dan 80 - 81 sesuai dengan modul praktikum) untuk mendaftarkan Middleware yang baru dibuat, yaitu “AgeMiddleware”, pada file bootstrap/app.php
   
<img width="940" alt="Screenshot 2023-11-08 123829" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9a66f477-02f4-4974-bfc6-467441b60442">

---

3. Menambahkan sintaks pada baris 72 - 78 sesuai dengan modul praktikum untuk menambahkan middleware pada routes dengan menambahkan opsi middleware pada salah satu route
   
<img width="941" alt="Screenshot 2023-11-08 123845" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e8b6b103-3b6c-4121-8b04-7e344718ddbe">

---

4. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/admin/home) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “Di bawah umur” disebabkan tidak diisinya parameter age
   
<img width="562" alt="Screenshot 2023-11-08 123907" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/73b9eeee-3544-42c0-9307-4daa2e831451">

---

5. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/admin/home?age=16) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “Di bawah umur” disebabkan terdapatnya function handle pada AgeMiddleware dimana (age < 17) akan mengembalikan return redirect (‘/fail’) pada web.php, yang nantinya akan menghasilkan output “Di bawah umur”
   
<img width="559" alt="Screenshot 2023-11-08 123956" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b47141e8-c1ba-47d1-8e0b-4025e4bc5a91">

---

6. Melakukan percobaan koneksi pada postman dengan menggunakan URL (http://localhost:8000/admin/home?age=18) dan method (get). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output “Dewasa” disebabkan parameter umur yang diisi telah melewati boundaries pada function handle Age Middleware, yaitu (age < 17)
   
<img width="560" alt="Screenshot 2023-11-08 124016" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/2e14e84c-bf4a-4dd3-930b-6634b43593b3">

---

### Kesimpulan Praktikum ###

1. Dynamic Route:
- Memahami konsep dynamic route, yaitu route yang dapat berubah-ubah.
- Menerapkan parameter pada routes (1 atau > 1 parameter) memungkinkan penggunaan variabel yang dinamis
- Menggunakan optional routes memberikan fleksibilitas, yang memungkinkan endpoint dipanggil dengan atau tanpa parameter variabel.

2. Aliases Route:
- Konsep aliases route digunakan untuk memberi nama pada route yang telah dibuat untuk membantu mempermudah pengelolaan route saat memanggilnya dalam aplikasi.

3. Group Route:
- Menerapkan grouping pada routes memungkinkan pengelompokkan route berdasarkan prefix tertentu.
- Selain prefix, pengguna juga dapat mengelompokkan middleware dan namespace pada kelompok routes.

4. Middleware:
- Secara konsep, middleware bersifat sebagai penengah antara komunikasi aplikasi dan client, yang sering digunakan untuk membatasi interaksi dengan aplikasi.
- Pada percobaan praktikum, praktikan diminta untuk membuat middleware Age yang memeriksa usia pengguna sebelum memproses permintaan.
- Pendaftaran middleware pada aplikasi dilakukan pada file bootstrap/app.php, yang menunjukkan cara mengatur middleware pada tingkat aplikasi.
- Penerapan middleware pada route tertentu memastikan bahwa filter hanya diterapkan pada route yang diinginkan.
