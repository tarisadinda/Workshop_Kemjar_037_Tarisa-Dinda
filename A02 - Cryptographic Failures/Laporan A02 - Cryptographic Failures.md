<div align='center'>
<h2>LAPORAN RESMI <br> PRAKTIKUM KEAMANAN JARINGAN <br> A02 – CRYPTOGRAPHIC FAILURES</h2>
<br><br><br>

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.001.png)

<br><br>
<b>Oleh :</b>

Tarisa Dinda Deliyanti - 3122640037 <br> Fisabili Maghfirona Firdaus - 3122640051 <br> D4 LJ Teknik Informatika B

<h2>POLITEKNIK ELEKTRONIKA NEGERI SURABAYA</h2>

<h2>TAHUN AJARAN 2022/2023</h2>
</div>
<br><br>

1. Untuk menguji cryptographic failures, akan mencoba mencari nested easter egg. Easter egg merupakan pesan tersembunyi yang telah disisipkan kedalam website. Untuk masuk ke direktori ftp, klik github pada menu di website Juice Shop. 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.002.jpeg)

2. Masuk ke direktori ftp kemudian cari file eastere.gg. Buka file tersebut dan perhatikan pesan pada file. 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.003.jpeg)

3. Klik file eastere.gg dan akan tampil pesan bahwa file tersebut bukan eastere.gg yang asli dan ada kode yang ditampilkan untuk menemukan easter egg. Jadi di dalam file tersebut muncul pesan enkripsi. Kita diharuskan memecahkan kode enkripsi tersebut. 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.004.jpeg)

4. Mengunjungi [ https://gchq.github.io/CyberChef/ ](https://gchq.github.io/CyberChef/) untuk  membuka  website  Cyber  Chef. Cyber Chef Aplikasi web sederhana dan intuitif untuk menganalisis dan mendekode data tanpa harus berurusan dengan alat atau bahasa pemrograman yang rumit. Copy kode dari file eastere.gg ke cyber chef 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.005.jpeg)

5. Tambahkan  base64 dan encryption ROT13. Setelah menambahkan base64 dan ROT13 kedalam recipe maka muncul link menuju file tersembunyi. 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.006.jpeg)
<br>Base64 adalah teknik pengkodean, yang mengubah data biner, seperti gambar dan video, menjadi format ASCII (skema pengkodean untuk merepresentasikan data teks dalam sistem komputer). Karena data biner terdiri dari string 0 dan 1, pengkodean Base64 bekerja dengan mengubah karakter ini menjadi himpunan ASCII yang pasti. Hasilnya dapat dengan mudah diterjemahkan dengan memetakan karakter ASCII ke dalam nilai biner. 

ROT 13 (Rotation 13) 

Salah satu contoh dari “substitution cipher” adalah Rot13. Metode rot13 merupakan metode enkripsi  yang mengubah suatu huruf menjadi huruf yang letaknya 13 posisi  dari huruf semula. Misalnya ‘A’ akan berubah menjadi ‘N’ , ‘B’ berubah menjadi ‘O’, dst. Rumusnya seperti dibawah ini : 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.007.png)

6. Hasil setelah menggabungkan alamat pesan tersembunyi dari website Juice Shop dan kode dipecahkan oleh cyber chef muncul teks link tambahkan link stelah port 3000. Maka akan muncul hasil seperti gambar di bawah ini 

![](Aspose.Words.b8a6d890-8893-40f2-9c73-9e21a91819f5.008.jpeg)

Link video presentasi OWASP A2 :[ https://youtu.be/61A7ucVB570](https://youtu.be/61A7ucVB570) 
