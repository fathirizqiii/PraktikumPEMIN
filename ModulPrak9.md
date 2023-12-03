# Praktikum 9 : JSON Web Token (JWT)

## Nama : Muhammad Fathi Rizqi ##
## NIM : 215150707111016 ##

### Tujuan Praktikum ###
1. Memahami konsep JWT
2. Mengimplementasikan authorization dengan JWT

##

### Dasar Teori Praktikum ###
1. JSON Web Token merupakan standar terbuka yang mendefinisikan cara ringkas dan mandiri untuk transmisi informasi antarpihak secara aman dalam bentuk objek JSON. Informasi ini dapat diverifikasi karena ditandatangani secara digital menggunakan secret key (dengan algoritma HMAC) atau pasangan kunci publik/pribadi menggunakan RSA atau ECSDA.
2. JSON Web Token dapat digunakan sebagai proses authorization (Setelah user masuk, setiap request perlu menyertakan. Hal ini mengizinkan user untuk mengakses route, service, dan resource yang diizinkan menggunakan token) dan information exchange (Berfungsi untuk mengamankan transmisi data antar pihak disebabkan JWT dapat ditandatangani untuk memastikan data dikirimkan oleh pengirim yang benar. Penggunaan signature yang dihitung dengan header dan payload dapat memverifikasi data yang dikirimkan tidak diubah di tengah jalan)
3. JSON Web Token menggunakan struktur dengan pola, berupa header, payload, dan signature dipisahkan dengan titik. Header berisikan algoritma yang digunakan serta jenis token, payload
berisikan data yang ditransmisikan, sedangkan signature merupakan hasil penandatanganan yang dilakukan dengan header dan payload yang sudah di-encode diikuti dengan secret key
menggunakan algoritma yang didefinisikan di header.
   
##

### Langkah Percobaan Praktikum ###

### A. Penyesuaian Database

1. Melakukan pengubahan fungsi up() pada file, yaitu menghapus parameter ‘72’ dan hanya menyisakan parameter ‘token’ di baris 15, seperti pada gambar

<img width="646" alt="Screenshot 2023-12-03 070745" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/aac7c25a-2623-4366-8cad-c498e7532757">

---

2. Menjalankan perintah “php artisan migrate:fresh” untuk memperbaharui migrasi dan menghapus data yang lama.

<img width="815" alt="Screenshot 2023-12-03 070802" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e8c70069-f929-4dac-a578-fdadb68b4010">

---

3. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/auth/register”, method “POST”, dan body ("name": "Scaramouche",
"email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (success), message (“New user created”), dan data user (name “Scaramouche”, email “scaramouche@fatui.org”, password, updated_at, created_at, id “1”)

<img width="668" alt="Screenshot 2023-12-03 070845" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a8032c94-5ffd-42f2-8c58-da980a139ffe">

---

### B. JWT Manual

1. Menambahkan sintaks pada baris 71 - 99 untuk menambahkan ketiga fungsi, yaitu base64url_encode, sign, dan jwt, pada File AuthController.php dalam folder app/Http/Controllers

<img width="668" alt="Screenshot 2023-12-03 070901" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3cd45204-a100-41bc-93a5-7ee1bdcbc710">

---

2. Melakukan pengubahan fungsi login pada file AuthController.php , yaitu menambahkan baris 62 - 73, seperti pada gambar
   
<img width="501" alt="Screenshot 2023-12-03 070925" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/339a01b8-aa4a-4cca-aa55-17fe42afb37a">

---

3. Menambahkan sintaks pada baris 38 - 70 untuk menambahkan keempat fungsi, yaitu base64url_encode, base64url_decode, sign, dan verify, pada File Authorization.php dalam folder app/Http/Middleware
   
<img width="641" alt="Screenshot 2023-12-03 070943" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b5ed7738-42da-4f56-986c-a778ab620a8a">

---

4. Melakukan pengubahan fungsi handle pada file Authorization.php seperti pada gambar
   
<img width="641" alt="Screenshot 2023-12-03 071000" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0967b037-a1ac-4178-a2bd-d16bbba1c593">

---

5. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/auth/login”, method “POST”, dan body ("email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (success), message (“Successfully login”), dan data user (id “1”,  created_at, updated_at, name “Scaramouche”, email “scaramouche@fatui.org”, password, token)
   
<img width="650" alt="Screenshot 2023-12-03 071047" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9c650fbd-dee0-4ed5-a274-7836a594eb07">

---

6. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/home”, method “GET”, dan body (Accept-Encoding “gzip, deflate, br”, Connection “keep-alive”, token). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (“Success”) dan message (“Selamat datang Scaramouche”)
   
<img width="641" alt="Screenshot 2023-12-03 071130" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5ca102fe-b595-427c-87d5-988d3fba5158">

---

### C. JWT Library

1. Melakukan proses generate jwt key secara online menggunakan website Djecrety ― Django Secret Key Generator. Terlihat pada gambar bahwa jwt key telah tergenerate, kemudian lakukan copy pada jwt key tersebut

<img width="813" alt="Screenshot 2023-12-03 071148" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/00ed32bb-2f1c-49db-bc38-c9c970b6b2b4">

---

2. Membuat variabel baru bernamakan “JWT_SECRET” pada file .env, kemudian memasukkan secret key yang didapat dari proses sebelumnya
   
<img width="697" alt="Screenshot 2023-12-03 071215" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/efe05506-8c0c-4a20-8d1f-2c0b8261ecbf">

---

3. Menjalankan perintah “composer require firebase/php-jwt” untuk melakukan instalasi package jwt firebase
   
<img width="711" alt="Screenshot 2023-12-03 071232" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9ddf0787-1ed0-4e97-8c44-4561251c51ef">

---

4. Menambahkan sintaks pada baris 18 - 21 untuk menambahkan fungsi, yaitu __construct, pada File AuthController.php dalam folder app/Http/Controllers
   
<img width="789" alt="Screenshot 2023-12-03 071249" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d110f755-750a-40a4-8c0d-123dc4791786">

---

5. Melakukan pengubahan fungsi login pada file AuthController.php , yaitu menambahkan baris 74, seperti pada gambar
   
<img width="551" alt="Screenshot 2023-12-03 071327" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5b7c8a76-458d-4e08-b341-84ed20fdf128">

--- 

6. Membuat File bernamakan “JwtMiddleware.php”, kemudian menambahkan sintaks sesuai dengan modul praktikum
   
<img width="512" alt="Screenshot 2023-12-03 071357" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/c3778adf-9b48-4b73-9059-fa0d32b5fc1b">

---

7. Mendaftarkan middleware yang telah dibuat pada bootstrap/app.php, yaitu pada baris 82
   
<img width="859" alt="Screenshot 2023-12-03 071416" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/338fa7fa-bf92-4add-b67e-508a2195b6a1">

---

8. Menambahkan sintaks pada baris 113 sesuai dengan modul praktikum pada File web.php dalam folder routes
   
<img width="797" alt="Screenshot 2023-12-03 071432" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/baf59c2f-a83f-4401-adfd-6258c640e6f7">

---

9. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/auth/login”, method “POST”, dan body ("email": "scaramouche@fatui.org", "password": "wanderer"). Terlihat pada gambar bahwa proses yang dijalankan berhasil dengan mengembalikan output terkait informasi status (“Success”), message (“Successfully login”), data user (id “1”, created_at, updated_at, name “Scaramouche”, email “scaramouche@fatui.org”, password, dan token).
    
<img width="628" alt="Screenshot 2023-12-03 071455" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/15961b43-fdf1-49b2-8fe6-43b76fbd20f4">

---

10. Melakukan pengaksesan aplikasi menggunakan Postman dengan URL “http://localhost:8000/home”, method “GET”, dan body (token) terkait informasi status (“Success”) dan message (“Selamat datang Scaramouche”)
    
<img width="616" alt="Screenshot 2023-12-03 071545" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/51ba453b-33d1-4147-9b3d-4ab58924bb02">

---

### Kesimpulan Praktikum ###

1. Penyesuaian Database:
- Penyesuaian dilakukan pada migrasi untuk menghapus parameter panjang kolom token.

2. JWT Manual:
- Menambahkan fungsi "base64url_encode", "base64url_decode", "sign", dan "verify" pada middleware "Authorization.php" untuk mengelola operasi encoding, decoding, penandatanganan, dan verifikasi JWT secara manual.
- Memperbarui fungsi login pada "AuthController.php" untuk menghasilkan JWT setelah login.
- Token yang dihasilkan setelah login dapat digunakan untuk otorisasi di endpoint tertentu.

3. JWT Library:
- Melakukan generate secret key secara online dan disimpan pada file ".env".
- Melakukan penginstalan library PHP-JWT dari Firebase menggunakan Composer.
- Menambahkan fungsi jwt pada "AuthController.php" untuk menghasilkan token JWT menggunakan library Firebase.
- Menambahkan middleware "JwtMiddleware.php" untuk mengelola otentikasi JWT menggunakan library Firebase.
- Mengaktifkan middleware pada route "/home" pada "file web.php".
- Melakukan pengujian dengan menjalankan permintaan login dan menggunakan token yang dihasilkan untuk mengakses endpoint yang memerlukan otentikasi.

4. Hasil Implementasi:
- Pengguna dapat melakukan registrasi dan login menggunakan endpoint "/auth/register" dan "/auth/login".
- Token JWT dihasilkan setelah login dan digunakan untuk mengakses endpoint yang memerlukan otorisasi, seperti "/home".
- Middleware JWT memastikan bahwa hanya permintaan yang menyertakan token yang valid yang dapat mengakses route "/home".
- Implementasi menggunakan library Firebase akan memudahkan proses otentikasi dan otorisasi dengan menyediakan fungsi-fungsi yang sudah terdefinisi
   
##
