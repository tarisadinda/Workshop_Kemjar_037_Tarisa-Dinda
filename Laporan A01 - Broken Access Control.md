**LAPORAN RESMI**

**PRAKTIKUM KEAMANAN JARINGAN**

**A01 – BROKEN ACCESS CONTROL**





![A picture containing logo

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.001.png)



**Oleh :**

**Tarisa Dinda Deliyanti		3122640037**

**Fisabili Maghfirona Firdaus	3122640051**

**D4 LJ Teknik Informatika B**



**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA**

**TAHUN AJARAN 2022/2023**



1. Menjalankan website Juice Shop menggunakan perintah “npm start” di dalam folder Juice Shop. Setelah port tersedia, kemudian membuka localhost:3000 ![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.002.png)
1. Berikut tampilan website yang ditampilkan di port 3000

![Graphical user interface, website

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.003.png)

1. Mencari alamat email admin melalui review yang ada di produk Apple Juice. Alamat email admin digunakan untuk mengecek broken access control. Dari gambar di bawah ini, didapatkan informasi bahwa email admin yaitu admin@juice-sh.op

![Graphical user interface, application, Teams

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.004.png)

1. Menjalankan aplikasi burpsuite. Kemudian buka Proxy lalu pilih Proxy Setting lalu pilih Project dan pilih Scope. Setelah muncul tampilan seperti berikut, tambahkan prefix alamat website yang akan dibuka yaitu localhost:3000 dengan mengklik tombol “Add” di bagian include in scope

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.005.png)

![Graphical user interface

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.006.jpeg)

1. Klik Tools, pilih Proxy, dan centang bagian yang diberi kotak berwarna merah seperti pada gambar berikut

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.007.png)![Graphical user interface, application

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.008.jpeg)

1. Mengubah intercept dari off ke on. Setelah itu, kembali ke halaman login Juice Shop dan masuk menggunakan email <admin@juice-sh.op> dan password acak![Graphical user interface

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.009.png)

Setelah klik tombol Login, kembali ke burpsuite dan di halaman Intercept klik “Forward” hingga bertemu informasi email dan password yang diinputkan sebelumnya

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.010.jpeg)

1. Klik kanan lalu pilih “Send to intruder” dan klik menu Intruder hingga muncul tampilan seperti gambar berikut

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.011.png)

1. Membersihkan target untuk semua burte force dengan menekan tombol “Clear$”

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.012.png)![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.013.png)

1. Pilih password sebagai target burte force dan klik tombol "Add$"

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.012.png)![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.012.png)![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.014.png)

1. Klik menu Payload di Intruder dan pilih file berformat .txt setelah klik tombol “Load”

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.015.png)![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.015.png)![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.016.png)

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.017.png)

1. Setelah file password.txt berhasil diload akan muncul tampilan yang berisi daftar password acak seperti berikut dan klik “Start attack” di pojok kanan

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.015.png)![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.018.png)

1. Berikut hasil setelah menekan tombol “Start attack”

![](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.019.png)![Table

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.020.png)

Terdapat dua macam HTTP status yaitu 401 yang berarti permintaan browser ke server tidak memiliki kredensial autentik yang valid dan 200 yang berarti server berhasil menerima request dari browser yang kita gunakan.

1. Login menggunakan password dengan status 200 untuk masuk ke akun admin

![Graphical user interface, application, Teams

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.021.png)

![Graphical user interface

Description automatically generated](Aspose.Words.f6e8d178-b69c-463d-ba3a-f8cd2178ba0d.022.png)

Link video presentasi OWASP A1 : <https://youtu.be/61A7ucVB570> 
