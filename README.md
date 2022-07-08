# Praktikum 11: PHP Framework (Codeigniter)

Nama    = Dian Tri Handayani

NIM     = 312010041

Kelas   = TI 20 D1

# Langkah-langkah Praktikum

1. Buat folder baru dengan nama lab11_php_ci pada docroot webserver (htdocs)

![WEB 2](https://user-images.githubusercontent.com/101880835/172562412-74d8e582-5cdf-4abf-be19-eb3048315761.png)


2. Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini


![WEB 3](https://user-images.githubusercontent.com/101880835/172562579-aabb30ed-c22a-4a6c-a580-e082e050b9d1.png)

3. Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.

![web 1](https://user-images.githubusercontent.com/101880835/172562088-7482d28c-b641-4014-8ecb-0e637374d786.png)

4. Instalasi Codeigniter 

Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual.

Unduh Codeigniter dari website https://codeigniter.com/download
Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.
Ubah nama direktory framework-4.x.xx menjadi ci4.
Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/

![halaman about terbaru](https://user-images.githubusercontent.com/101880835/178067351-d49b4674-5eb6-4996-8f65-1fe9761e5b85.png)
![halaman about](https://user-images.githubusercontent.com/101880835/178067361-1db34718-1d19-4953-a995-d5e8eb36a272.png)
![ini halaman term of service](https://user-images.githubusercontent.com/101880835/178067384-59502a67-d51d-4e77-b95c-e94123574ca0.png)
![router false true](https://user-images.githubusercontent.com/101880835/178067407-4a0f3cd1-9264-47d2-bb85-1ac76aeb53d3.png)

![envirenment](https://user-images.githubusercontent.com/101880835/178067520-cdcc2ce6-b235-4d5f-834d-f46eb1ca34ad.png)
![welcome](https://user-images.githubusercontent.com/101880835/178067596-1a91bdd1-03ce-4be8-8d5a-07fb3f564961.png)
![header php](https://user-images.githubusercontent.com/101880835/178067690-36bd9995-f62b-4a28-be74-eff8e0f2c3ad.png)
![MEMBUAT LAYOUT WEB BUAT FOLDER](https://user-images.githubusercontent.com/101880835/178067766-6462405d-0eb5-48fe-a5b9-b13c4b963380.png)
![page tmbh tulisan panjang](https://user-images.githubusercontent.com/101880835/178067794-76dad09f-2a7d-425f-a3b3-cdf7488fe511.png)
![view yg isi](https://user-images.githubusercontent.com/101880835/178067840-4a9f1d71-3e6f-4e25-b286-9347ccd02797.png)
![debugging home,php](https://user-images.githubusercontent.com/101880835/178067910-14843c37-3e9e-4573-8b56-dfdc67aaed66.png)




5. Menjalankan CLI (Command Line Interface)

Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt. Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (xampp/htdocs/lab11_php_ci/ci4/). Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah: php spark.


![xampp CLI](https://user-images.githubusercontent.com/101880835/178067554-f0fcd017-6995-4ae4-ad01-ecee2d72a55b.png)


6. Mengaktifkan Mode Debugging

Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.


![mengaktifkan mode debugging whoops](https://user-images.githubusercontent.com/101880835/178067335-480329bb-8efa-43cf-981f-4d0e353a7559.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. Kemudian mengubah nama file env menjadi .env lalu setelah itu buka file tersebut dan ubah nilai variable CI_ENVORNMENT menjadi development. Setelah itu hapus tanda tagar (#) pada awal baris CI_ENVIRONMENT, ubah kode pada file app/Controller/Home.php hilangkan titik koma (;) pada akhir kode seperti berikut.

![home ; ilang](https://user-images.githubusercontent.com/101880835/178067541-8ddf37d7-11e9-49cb-a1ec-a7ad2bbaf7eb.png)


![debugging env](https://user-images.githubusercontent.com/101880835/178067895-beac6072-cc21-4109-874a-d7d9d9211721.png)

Maka hasilnya akan terjadi error seperti berikut.

![pharse eror](https://user-images.githubusercontent.com/101880835/178067486-0e28afa5-62bc-4e3b-ad18-fa46d4858b48.png)


7. Routing dan Controller

Router terletak pada file app/config/Routes.php. Pada file tersebut kita dapat mendefinisikan route untuk aplikasi yang kita buat.

Contoh: $routes->get('/', 'Home::index'); Kode tersebut akan mengarahkan rute untuk halaman home.


8. Membuat Route Baru.

Tambahkan kode berikut di dalam Routes.php

![membuat roter baru, router php](https://user-images.githubusercontent.com/101880835/178067646-1ee793ed-2565-4f01-b825-517716ada7f6.png)


Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah berikut. php spark routes

![router cmd php spark](https://user-images.githubusercontent.com/101880835/178067466-d63177c2-b851-4c3c-ae21-663de4aab565.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about


![membuat router baru 404 not found](https://user-images.githubusercontent.com/101880835/178067311-1105312f-1c03-4939-a569-4f8e92546ca3.png)


Ketika diakses akan mucul tampilan error 404 file not found, itu artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

9. MEMBUAT CONTROLLER

Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.

![membuat controller page php](https://user-images.githubusercontent.com/101880835/178067868-a55de129-3066-4aab-ba7f-83c4bf5450f8.png)

Selanjutnya refresh Kembali browser, maka akan ditampilkan hasilnya yaitu halaman sudah dapat diakses.

![ini halaman about](https://user-images.githubusercontent.com/101880835/178067437-daf6a285-0914-4d8f-869f-0ed60ed94c53.png)


10. AUTO ROUTING 

Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true menjadi false.

Tambahkan method baru pada Controller Page seperti berikut

![AUTO ROTING PAGE PHP](https://user-images.githubusercontent.com/101880835/178067858-ca416d40-b6a2-4ec6-8a98-fe02ae1f2d6a.png)

Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos

![ini halaman term of service](https://user-images.githubusercontent.com/101880835/178067384-59502a67-d51d-4e77-b95c-e94123574ca0.png)

11. MEMBUAT VIEW

Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut.

![MEMBUAT VIEW ABOUT PHP](https://user-images.githubusercontent.com/101880835/178067816-5e2b3146-fbe5-4d06-a34d-e5c9857deab9.png)

Ubah method about pada class Controller Page menjadi seperti berikut:

![MEMBUAT VIEW UBAH PAGE PHP](https://user-images.githubusercontent.com/101880835/178067781-6550d61b-c340-48a9-a848-a876972808f5.png)

Kemudian lakukan refresh pada halaman tersebut.


![halaman about](https://user-images.githubusercontent.com/101880835/178067361-1db34718-1d19-4953-a995-d5e8eb36a272.png)


12. MEMBUAT LAYOUT WEB DENGAN CSS

Pada dasarnya layout web dengan css dapat diimplamentasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public.

Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout. Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![file style di folder](https://user-images.githubusercontent.com/101880835/178067741-c48ab08b-0b4d-4783-ac86-49f39d3a6ef5.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php

File app/view/template/header.php

![MEMBUAT LAYOUT HEADER PHP](https://user-images.githubusercontent.com/101880835/178067715-f3a72dfd-0c61-45e2-8e4e-584f957c4245.png)

File app/view/template/footer.php

![footer php](https://user-images.githubusercontent.com/101880835/178067678-523699aa-67b6-47df-a184-351a00735965.png)

Kemudian ubah file app/view/about.php seperti berikut.

![about php terbaru](https://user-images.githubusercontent.com/101880835/178067661-f034ac98-8029-4bca-a3a6-b0e0e24dbed6.png)

Selanjutnya refresh tampilan pada alamat http://localhost:8080/about
![halaman about terbaru](https://user-images.githubusercontent.com/101880835/178067351-d49b4674-5eb6-4996-8f65-1fe9761e5b85.png)

