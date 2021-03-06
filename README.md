# Final Project

#### Tahap 1 Instalasi Laravel

1. Sebelum melakukan instalasi laravel, **pastikan anda sudah menginstall Xampp dan Composer**

1. Langkah pertama dalam install Laravel adalah masuk ke Command Prompt, dengan cara klik Win+R lalu ketik cmd dan klik **OK**

   ![](laravel/1.PNG)

2. Sebelum melakukan instalasi Laravel, arahkan Command Prompt atau terminal menuju direktori file server. Lokasi file server pada XAMPP secara default berada pada direktori xampp/htdocs. Masukan perintah ini pada jendela Command Prompt untuk masuk ke direktori htdocs.

   ```markdown
   cd \xampp\htdocs
   ```

![](laravel/2.PNG)

3. Selanjutnya jika sudah masuk direktori htdocs, Anda harus membuat request untuk mengambil (serta menginstall) file Laravel yang telah disediakan dalam repositori Github. Gunakan perintah ini untuk melakukan request:

   ```markdown
   composer create-project --prefer-dist laravel/laravel nama_projectmu
   ```

   Jika perintah telah berhasil dimasukkan, Composer akan mulai melakukan proses pengambilan data serta instalasi Laravel ke dalam direktori yang telah Anda tentukan. Pastikan bahwa koneksi internet dalam keadaan stabil agar tidak terjadi gangguan pada saat proses pengambilan data Laravel.

![](laravel/3.PNG)

4. Setelah proses download file Laravel selesai, nantinya akan ada folder baru pada direktori file server dengan nama sesuai nama project yang telah Anda tentukan sebelumnya pada folder /xampp/htdocs.

![](laravel/4.PNG)

​	Untuk memastikan bahwa Laravel sukses terinstall dan siap untuk digunakan, arahkan Command Prompt atau Terminal menuju direktori yang telah Anda buat sebelumnya. Lalu, masukkan perintah berikut ke dalam Command Prompt atau Terminal:

```markdown
php artisan serve
```

![](laravel/a.PNG)

5. Jika muncul tulisan Laravel development server started pada Command Prompt atau Terminal, langkah selanjutnya adalah membuka link yang telah disediakan oleh Laravel. Secara default, Anda akan diarahkan menuju alamat server,yaitu 127.0.0.1:8000. Nantinya, akan muncul tampilan homepage dengan tulisan Laravel di bagian tengah seperti pada gambar di bawah ini:

   ![](laravel/5.PNG)

### **Tahap 2 RSS**

1. Langkah pertama, ubah nama DB_DATABASE di .env sesuai dengan nama database yang sudah dibuat di php my admin

   ![](Rss/1.PNG)

   ![](Rss/2.PNG)

2. Buat file RssController.php dan NewsController.php di app/http/controllers

   ``` 
   php artisan make:controller RSSController
   php artisan make:controller NewsController
   ```

3. Coba jalankan migration dan seeding dengan perintah berikut :

   ```
   php artisan migrate:fresh
   php artisan migrate --seed
   ```

4. Setelah sukses menjalankan perintah 3, lanjutkan dengan edit file di NewsController.php

   ![](Rss/3.PNG)

   ![](Rss/4.PNG)

5. Jika sudah berhasil menjalankan perintah sebelumnya, tambahkan sebuah Route di web.php

   ![](Rss/5.PNG)

6. Cek database di php my admin, untuk melihat apakah sudah terupdate atau belum

   ![](Rss/6.PNG)

   ![](Rss/7.PNG)

7. Langkah terakhir lakukan pengecekan RSS apakah sudah berhasil atau belum

   ![](Rss/8.PNG)

#### Tahap 3 Tampilan Halaman RSS
Berikut ditampilkan halaman RSS yang telah dibuat
![Tampilan RSS](https://user-images.githubusercontent.com/95134218/178119434-7104737c-6857-44f2-95a6-0baba04f3699.PNG)
Berikut Link RSS yang digunakan :
1. https://news.un.org/feed/subscribe/en/news/topic/climate-change/feed/rss.xml
2. https://news.un.org/feed/subscribe/en/news/topic/women/feed/rss.xml
3. https://news.un.org/feed/subscribe/en/news/topic/culture-and-education/feed/rss.xml
