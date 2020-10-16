# Jarkom_Modul1_Lapres_A04

- I Gusti Agung Chintya Prema Dewi<br />
05111840000130
- Kholilah Zaki Lismia <br />
05111840000

### No. 1
---------------------------
**Sebutkan webserver yang digunakan pada "testing.mekanis.me"!**
```bash
http.host == testing.mekanis.me
```
Display capture ```http.host``` digunakan ketika ingin menampilkan paket http dengan nama host yang diinginkan, dalam hal ini yang dicari adalah paket dengan host ```testing.mekanis.me```. Setelah mendapatkan paket yang diinginkan, cari detail dari paket menggunakan ```follow``` lalu ke bagian ```http stream```. Akan didapatkan detail paket seperti ini :
<p align="center"><img width="221" alt="j_1" src="https://user-images.githubusercontent.com/62136051/96267660-a9351100-0ffa-11eb-8948-581678f183bb.png"></p>

Dalam detail tersebut terdapat keterangan web server yang digunakan web ```testing.mekanis.me``` adalah nginx/1.14.0 (Ubuntu)

### No. 2
-----------------------------
**Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!**
```bash
http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"
```
<p align="center"><img width="490" alt="Screen Shot 2020-10-17 at 00 51 48" src="https://user-images.githubusercontent.com/62136051/96286431-f1602d80-1012-11eb-9f4d-57bb77d20b71.png"></p>

Untuk menyimpan gambar yang diminta, pertama-tama harus dilakukan display filter agar yang ditampilkan hanya paket yang berisi gambar yang diminta. Setelah itu paket tersebut di export dan disimpan.

<p align="center"><img width="376" alt="Screen Shot 2020-10-17 at 00 52 17" src="https://user-images.githubusercontent.com/62136051/96286475-0210a380-1013-11eb-8bae-710ce805d46a.png"></p>

Berikut adalah gambar yang diminta

<p align="center"><img width="376" src="https://user-images.githubusercontent.com/62136051/96287009-da6e0b00-1013-11eb-96fd-2095ec1fc37f.jpg"></p>


### No. 3
-------------------------------
**Cari username dan password ketika login di "ppid.dpr.go.id"!**
```bash
http.request.method == POST
```
Display picture ```http.request.method``` bermaksud untuk menampilkan paket http dengan ```POST``` request karena ketika login, berarti user mem-POST username dan password. Username dan Password tersebut dapat dilihat didalam ```Hyepertext Transfer Protocol```
<p align="center"><img width="497" alt="j_3" src="https://user-images.githubusercontent.com/62136051/96265449-05e2fc80-0ff8-11eb-9c04-a9ead45e33d2.png"></p>

Berdasarkan data tersebut **username: 10pemuda** dan **password: guncangdunia**

### No. 5
---------------------------------
**Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!**

Pada saat memasuki web ```aku.pengen.pw``` dibutuhkan *username* dan *password*, oleh karena itu pertama-tama harus dicari *username* dan *passwordnya* melalui wireshark. 

<p align="center"><img width="425" alt="j_5_1" src="https://user-images.githubusercontent.com/62136051/96272117-3fb80100-1000-11eb-978e-8dbdd926ca7f.png"></p>

Karena web ```aku.pengen.pw``` menggunakan *basic authentication* maka dari itu digunakan display picture ```http contains "Authorization: Basic"``` dan kita juga mencari paket yang memiliki host ```aku.pengen.pw``` jadi kita gunakan ```http contains "aku.pengen.pw"```. Dalam foto diatas bisa dilihat bagian ```Hypertext Transfer Protocol``` dan sub bagiannya ```Authorization``` ada section ```credentials``` yang menyatakan ***username:password*** berarti **username: kakakgamtenk** dan **password: hartatahtabermuda**

Setelah login akan terlihat halaman seperti ini 

<p align="center"><img width="425,5" alt="j_5_2" src="https://user-images.githubusercontent.com/62136051/96272037-28791380-1000-11eb-9a4b-1726e24963c2.png"></p>

### No. 8
--------------------------------

**Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!**
 Langkah pertama yang harus dilakukan adalah mencari paket yang berasal dari koneksi FTP dengan Microsoft FTP Service. Langkah ini dilakukan menggunakan display capture ```ftp contains "Microsoft"```.
 
 <p align="center"><img width="493,5" alt="8_1" src="https://user-images.githubusercontent.com/62136051/96280061-156b4100-100a-11eb-91f3-831910a7efe4.png"></p>
 
 Setelah mendapatkan IP address dari Microsoft FTP Service, kita display capture lagi untuk mencari objek apa saja yang didownload menggunakan command ```RETR```. Dan didapatkan hasil seperti ini
 
 <p align="center"><img width="493,5" alt="8_2" src="https://user-images.githubusercontent.com/62136051/96280048-10a68d00-100a-11eb-943c-a28a91d30dcc.png"></p>
 
### No. 9
----------------------------------

**Cari username dan password ketika login FTP pada localhost!**
```bash
ftp && ftp.request.command == PASS || ftp.request.command == USER
```

<p align="center"><img width="489" alt="Screen Shot 2020-10-17 at 00 26 27" src="https://user-images.githubusercontent.com/62136051/96283875-692c5900-100f-11eb-8dac-96354612bc59.png"></p>

Karena protokol yang digunakan adalah FTP maka digunakan display capture ```ftp``` dan yang diminta adalah username dan password, jadi digunakan display capture  ```ftp.request.command == PASS || ftp.request.command == USER```

### No. 11
-------------------------------
**Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!**
```bash
port 21
```
<p align="center"><img width="632,25" alt="Screen Shot 2020-10-17 at 00 30 47" src="https://user-images.githubusercontent.com/62136051/96284320-025b6f80-1010-11eb-8dd9-827177120794.png"></p>

```Port 21``` merupakan port untuk localhost, jadi untuk membuktikannya harus ada aktivitas dari localhost, disini saya mencoba mengaktifkan koneksi ftp.

### No. 12
--------------------------------
**Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!**

```bash
src port 80
```

<p align="center"><img width="409" alt="Screen Shot 2020-10-17 at 00 35 26" src="https://user-images.githubusercontent.com/62136051/96284777-a80ede80-1010-11eb-8817-831fe6c76e46.png"></p>

```src port 80``` merupakan capture filter untuk menangkap semua paket yang berasal dari port 80, disini kami membuktikan dengan mengakses suatu web dengan berasal dari port 80.

### No. 13
------------------------------------------
**Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!**
```bash
dst port 443
```
<p align="center"><img width="465,5" alt="Screen Shot 2020-10-17 at 00 40 54" src="https://user-images.githubusercontent.com/62136051/96285352-6cc0df80-1011-11eb-80b1-e84edde65dbd.png"></p>

```dst``` dalam ```dst port``` berarti ```destination``` yang mana berarti akan menangkap semua paket yang menuju ke port 443. 

### No. 15
-----------------------------------------
**Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!**
```bash
Dst host monta.if.its.ac.id
```

<p align="center"><img width="425,5" alt="Screen Shot 2020-10-17 at 00 45 19" src="https://user-images.githubusercontent.com/62136051/96285829-09837d00-1012-11eb-814f-594f673d4242.png"></p>

Sama seperti nomor 13, ```dst``` dalam ```Dst host monta.if.its.ac.id``` berarti ```Destination``` yang mana keseluruhan capture nya bermaksud hanya menangkap paket yang tujuannya ke monta.if.ac.id.


