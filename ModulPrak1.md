# Praktikum 1 : Instalasi Lumen, MongoDB, dan Konfigurasi App Key 

### Nama : Muhammad Fathi Rizqi ###
### NIM : 215150707111016 ###

1. Melakukan instalasi Composer dan MongoDB berdasarkan sumber download yang telah disediakan pada modul praktikum
(Composer : https://getcomposer.org/download/, MongoDB : https://www.mongodb.com/try/download/community dan)

<img width="654" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e3d662b8-543b-4514-835a-344eeed4b2f8">
<img width="526" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9e60ddd7-8c70-4b8e-b2ca-e17f541a2ab4">

....

2. Menjalankan mongodb-windows-x86_64-6.0.1-signed.msi yang telah diinstall sebelumnya. (Saya telah melakukan instalasi Composer dan MongoDB sebelumnya sehingga tahapan penginstallannya sedikit berbeda dengan modul. Tahapan yang saya lakukan adalah "change" disebabkan sudah terinstallnya MongoDB ini, tetapi memiliki tujuan untuk menginstall MongoDB. Pengguna cukup menggunakan konfigurasi aplikasi secara default dan mencentang End-User License Agreement untuk dapat menginstall perangkat lunak ini. Nantinya, MongoDB akan secara otomatis terbuka setelah berhasil diinstall)
   
<img width="654" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/e73d4324-4502-435d-8de4-0573935588d9">
<img width="654" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/0da29680-4e04-4eac-9a72-d07adcdc73d0">
<img width="652" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/6a8a8ddf-a976-44f2-a92f-d28954a3af7a">
<img width="655" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/14295f62-ed5f-42a7-a0a7-9070852c8128">
<img width="653" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/c5d93ff0-3331-4896-80d3-d7d3653e0c69">
<img width="799" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/94b8f2ac-43f8-4075-8bfc-442515ed90ee">

....

3. Melakukan instalasi Lumen dengan membuka Command Prompt. Kemudian, copykan dan masuk ke direktori folder yang diinginkan (penggunaan perintah cd) sebagai wadah tempat menyimpan kebutuhan dari instalasi Lumen. Setelah itu, jalankan perintah "composer create-project --prefer-dist laravel/lumen lumenapi" untuk melakukan penginstallan pada folder yang telah ditentukan. Masuk ke folder projek dengan perintah "cd lumenapi", dan diakhiri dengan perintah "php -S localhost:8000 -t public" untuk menjalankan Server Lumen
<img width="733" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/2e66f51a-aa3e-428a-9de9-ec9f74c33996">
<img width="803" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/20d3a6c3-9f64-4365-bd8c-8114a5494cf5">
<img width="779" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/9695519c-f30d-4574-ae7e-853fe69bba98">

....

4. Langkah terakhir, yaitu melakukan konfigurasi App Key Lumen. Buatlah endpoint untuk mengembalikan random string dengan panjang 32 pada file web.php folder routes. Setelah itu, masukkan random string pada bagian App Key file .env (Saya telah mendapatkan random string sebelumnya melalui website "https://pinetools.com/random-string-generator"
<img width="694" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/bd1905e0-95b5-4d41-bafc-29e5e26bba69">
<img width="457" alt="image" src="https://github.com/fathirizqiii/PraktikumPEMIN/assets/103505061/23587ea7-75cd-44de-ba1b-a8b26cb9fe1b">

....






















