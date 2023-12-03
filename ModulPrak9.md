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

### A. Register

1. 

---


<img width="646" alt="Screenshot 2023-12-03 070745" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/aac7c25a-2623-4366-8cad-c498e7532757">
<img width="815" alt="Screenshot 2023-12-03 070802" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e8c70069-f929-4dac-a578-fdadb68b4010">
<img width="668" alt="Screenshot 2023-12-03 070845" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a8032c94-5ffd-42f2-8c58-da980a139ffe">
<img width="668" alt="Screenshot 2023-12-03 070901" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/3cd45204-a100-41bc-93a5-7ee1bdcbc710">
<img width="501" alt="Screenshot 2023-12-03 070925" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/339a01b8-aa4a-4cca-aa55-17fe42afb37a">
<img width="641" alt="Screenshot 2023-12-03 070943" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/b5ed7738-42da-4f56-986c-a778ab620a8a">
<img width="641" alt="Screenshot 2023-12-03 071000" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0967b037-a1ac-4178-a2bd-d16bbba1c593">
<img width="650" alt="Screenshot 2023-12-03 071047" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9c650fbd-dee0-4ed5-a274-7836a594eb07">
<img width="641" alt="Screenshot 2023-12-03 071130" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5ca102fe-b595-427c-87d5-988d3fba5158">
<img width="813" alt="Screenshot 2023-12-03 071148" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/00ed32bb-2f1c-49db-bc38-c9c970b6b2b4">
<img width="697" alt="Screenshot 2023-12-03 071215" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/efe05506-8c0c-4a20-8d1f-2c0b8261ecbf">
<img width="711" alt="Screenshot 2023-12-03 071232" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9ddf0787-1ed0-4e97-8c44-4561251c51ef">
<img width="789" alt="Screenshot 2023-12-03 071249" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d110f755-750a-40a4-8c0d-123dc4791786">
<img width="551" alt="Screenshot 2023-12-03 071327" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/5b7c8a76-458d-4e08-b341-84ed20fdf128">
<img width="512" alt="Screenshot 2023-12-03 071357" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/c3778adf-9b48-4b73-9059-fa0d32b5fc1b">
<img width="859" alt="Screenshot 2023-12-03 071416" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/338fa7fa-bf92-4add-b67e-508a2195b6a1">
<img width="797" alt="Screenshot 2023-12-03 071432" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/baf59c2f-a83f-4401-adfd-6258c640e6f7">
<img width="628" alt="Screenshot 2023-12-03 071455" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/15961b43-fdf1-49b2-8fe6-43b76fbd20f4">
<img width="616" alt="Screenshot 2023-12-03 071545" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/51ba453b-33d1-4147-9b3d-4ab58924bb02">



### Kesimpulan Praktikum ###

1. JSON Web Token (JWT):

Konsep JWT: Mahasiswa diharapkan memahami konsep dasar JWT, yaitu standar terbuka untuk transmisi informasi antar pihak secara aman dalam bentuk objek JSON.
Penggunaan JWT:
Setiap permintaan setelah user login harus menyertakan token.
JWT dapat digunakan untuk mengamankan transmisi data antar pihak dengan memastikan keaslian dan integritas data.
Struktur JWT:

JWT menggunakan format XXXXX.YYYYY.ZZZZZ yang terdiri dari header, payload, dan signature.
Header berisi algoritma yang digunakan dan jenis token.
Payload berisi data yang ditransmisikan.
Signature adalah hasil penandatanganan menggunakan secret key.
Langkah Percobaan:

Penyesuaian Database:

Penyesuaian dilakukan pada migrasi untuk menghapus parameter panjang kolom token.
JWT Manual:

Fungsi base64url_encode, base64url_decode, sign, dan verify ditambahkan pada middleware Authorization.php untuk mengelola operasi encoding, decoding, penandatanganan, dan verifikasi JWT secara manual.
Fungsi login pada AuthController.php diperbarui untuk menghasilkan JWT setelah login.
Token yang dihasilkan setelah login dapat digunakan untuk otorisasi di endpoint tertentu.
JWT Library:

Secret key di-generate secara online dan disimpan di file .env.
Library PHP-JWT dari Firebase diinstal menggunakan Composer.
Fungsi jwt ditambahkan pada AuthController.php untuk menghasilkan token JWT menggunakan library Firebase.
Middleware JwtMiddleware.php ditambahkan untuk mengelola otentikasi JWT menggunakan library Firebase.
Middleware diaktifkan pada route /home pada file web.php.
Pengujian dilakukan dengan menjalankan permintaan login dan menggunakan token yang dihasilkan untuk mengakses endpoint yang memerlukan otentikasi.
Hasil Implementasi:

Pengguna dapat melakukan registrasi dan login menggunakan endpoint /auth/register dan /auth/login.
Token JWT dihasilkan setelah login dan digunakan untuk mengakses endpoint yang memerlukan otorisasi, seperti /home.
Middleware JWT memastikan bahwa hanya permintaan yang menyertakan token yang valid yang dapat mengakses route /home.
Implementasi menggunakan library Firebase memudahkan proses otentikasi dan otorisasi dengan menyediakan fungsi-fungsi yang sudah terdefinisi
   
##
