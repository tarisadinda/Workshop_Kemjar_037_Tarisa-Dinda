<div align='center'>
<h2>LAPORAN RESMI <br> PRAKTIKUM KEAMANAN JARINGAN <br> A01 – BROKEN ACCESS CONTROL</h2>

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.001.png)

<h2>Oleh :</h2>

<h2>Tarisa Dinda Deliyanti  3122640037 <br> Fisabili Maghfirona Firdaus  3122640051 <br> D4 LJ Teknik Informatika B</h2>

<h2>POLITEKNIK ELEKTRONIKA NEGERI SURABAYA</h2>

<h2>TAHUN AJARAN 2022/2023</h2>
</div>

1. Menjalankan website Juice Shop menggunakan perintah “npm start” di dalam folder Juice  Shop.  Setelah  port  tersedia,  kemudian  membuka  localhost:3000

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.002.jpeg)

2. Berikut tampilan website yang ditampilkan di port 3000 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.003.jpeg)

3. Mencari alamat email admin melalui review yang ada di produk Apple Juice. Alamat email admin digunakan untuk mengecek broken access control. Dari gambar di bawah ini, didapatkan informasi bahwa email admin yaitu admin@juice-sh.op 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.004.jpeg)

4. Menjalankan  aplikasi burpsuite. Kemudian buka Proxy lalu pilih Proxy Setting lalu pilih  Project  dan pilih  Scope. Setelah  muncul  tampilan  seperti berikut,  tambahkan prefix alamat website yang akan dibuka yaitu localhost:3000 dengan mengklik tombol “Add” di bagian include in scope 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.005.jpeg)

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.006.jpeg)

5. Klik Tools, pilih Proxy, dan centang bagian yang diberi kotak berwarna merah seperti pada gambar berikut 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.007.png)

6. Mengubah intercept dari off ke on. Setelah itu, kembali ke halaman login Juice Shop dan  masuk  menggunakan  email [ admin@juice-sh.op ](mailto:admin@juice-sh.op) dan  password  acak

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.008.jpeg)

Setelah  klik  tombol  Login,  kembali  ke  burpsuite  dan  di  halaman  Intercept  klik “Forward” hingga bertemu informasi email dan password yang diinputkan sebelumnya 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.009.jpeg)

7. Klik kanan lalu pilih “Send to intruder” dan klik menu Intruder hingga muncul tampilan seperti gambar berikut 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.010.jpeg)

8. Membersihkan target untuk semua burte force dengan menekan tombol “Clear$” 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.011.png)

9. Pilih password sebagai target burte force dan klik tombol "Add$" 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.012.png)![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.013.png)

10. Klik menu Payload di Intruder dan pilih file berformat .txt setelah klik tombol “Load” 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.014.png)

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.015.jpeg)

11. Setelah  file password.txt berhasil  diload akan  muncul  tampilan  yang  berisi  daftar password acak seperti berikut dan klik “Start attack” di pojok kanan 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.016.png)

12. Berikut hasil setelah menekan tombol “Start attack” 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.017.png)

Terdapat dua macam HTTP status yaitu 401 yang berarti permintaan browser ke server tidak memiliki  kredensial  autentik yang valid dan 200 yang berarti  server berhasil menerima request dari browser yang kita gunakan. 

13. Login menggunakan password dengan status 200 untuk masuk ke akun admin 

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.018.jpeg)

![](Aspose.Words.7d7e684d-01f3-4432-8b3e-c6ddd947b64a.019.jpeg)

Link video presentasi OWASP A1 :[ https://youtu.be/61A7ucVB570](https://youtu.be/61A7ucVB570)  
