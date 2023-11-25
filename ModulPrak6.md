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

2. 
<img width="793" alt="Screenshot 2023-11-08 124333" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/286c4bfd-89d1-4b8b-ac55-67a1c7ae3c45">
<img width="791" alt="Screenshot 2023-11-08 124352" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f3e4374b-6765-4d92-bf74-76b69ac82047">
<img width="794" alt="Screenshot 2023-11-08 124407" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/24f238ec-91d9-4946-9ce8-dfc5e9c29dfd">
<img width="692" alt="Screenshot 2023-11-08 124428" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/78ac5038-0752-48d9-9115-46743d0c4032">
<img width="584" alt="Screenshot 2023-11-08 124450" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/4c1ba1ab-308a-4eaf-9ac4-75a33cff9066">
<img width="880" alt="Screenshot 2023-11-08 124505" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/70789dec-f293-4dfb-a105-0cf3860bb264">
<img width="906" alt="Screenshot 2023-11-08 124523" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/a35fd572-402a-4632-bea0-c0d20037035f">
<img width="908" alt="Screenshot 2023-11-08 124538" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/f16854dd-888e-4b88-a831-94044edf6730">
<img width="572" alt="Screenshot 2023-11-08 124559" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/03afd55c-fc17-4e8a-886b-fddf95cdcd98">
<img width="823" alt="Screenshot 2023-11-08 124613" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/af2a2063-6e43-40b5-9a60-f443d1f2dbbb">
<img width="806" alt="Screenshot 2023-11-08 124628" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/461d9c5d-daf9-405e-880d-eac213c55500">
<img width="950" alt="Screenshot 2023-11-08 124645" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/d05a857c-48e8-4a25-87a6-5b6f4a5f0083">
<img width="650" alt="Screenshot 2023-11-08 124708" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/06a3b282-a355-4d5d-a151-e6a05cc26cc7">
<img width="659" alt="Screenshot 2023-11-08 124727" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/71e43997-b776-4e23-bcb1-827d9563e9a6">
<img width="651" alt="Screenshot 2023-11-08 124744" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/18942a09-b2f5-4754-85ad-6a7c7823a9b4">
