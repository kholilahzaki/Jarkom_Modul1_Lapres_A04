# Jarkom_Modul1_Lapres_A04

- I Gusti Agung Chintya Prema Dewi<br />
05111840000130
- Kholilah Zaki Lismia <br />
05111840000

### No. 1
---------------------------
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
```bash
http.host == testing.mekanis.me
```
Display capture ```http.host``` digunakan ketika ingin menampilkan paket http dengan nama host yang diinginkan, dalam hal ini yang dicari adalah paket dengan host ```testing.mekanis.me```. Setelah mendapatkan paket yang diinginkan, cari detail dari paket menggunakan ```follow``` lalu ke bagian ```http stream```. Akan didapatkan detail paket seperti ini :
<p align="center"><img width="221" alt="j_1" src="https://user-images.githubusercontent.com/62136051/96267660-a9351100-0ffa-11eb-8948-581678f183bb.png"></p>

Dalam detail tersebut terdapat keterangan web server yang digunakan web ```testing.mekanis.me``` adalah nginx/1.14.0 (Ubuntu)

### No. 3
-------------------------------
Cari username dan password ketika login di "ppid.dpr.go.id"!
```bash
http.request.method == POST
```
Display picture ```http.request.method``` bermaksud untuk menampilkan paket http dengan ```POST``` request karena ketika login, berarti user mem-POST username dan password. Username dan Password tersebut dapat dilihat didalam ```Hyepertext Transfer Protocol```
<p align="center"><img width="497" alt="j_3" src="https://user-images.githubusercontent.com/62136051/96265449-05e2fc80-0ff8-11eb-9c04-a9ead45e33d2.png"></p>

Berdasarkan data tersebut **username: 10pemuda** dan **password: guncangdunia**

### No. 5
---------------------------------
Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

Pada saat memasuki web ```aku.pengen.pw``` dibutuhkan *username* dan *password*, oleh karena itu pertama-tama harus dicari *username* dan *passwordnya* melalui wireshark. 

<p align="center"><img width="425" alt="j_5_1" src="https://user-images.githubusercontent.com/62136051/96272117-3fb80100-1000-11eb-978e-8dbdd926ca7f.png"></p>

Karena web ```aku.pengen.pw``` menggunakan *basic authentication* maka dari itu digunakan display picture ```http contains "Authorization: Basic"``` dan kita juga mencari paket yang memiliki host ```aku.pengen.pw``` jadi kita gunakan ```http contains "aku.pengen.pw"```. Dalam foto diatas bisa dilihat bagian ```Hypertext Transfer Protocol``` dan sub bagiannya ```Authorization``` ada section ```credentials``` yang menyatakan ***username:password*** berarti **username: kakakgamtenk** dan **password: hartatahtabermuda**

Setelah login akan terlihat halaman seperti ini 

<p align="center"><img width="425,5" alt="j_5_2" src="https://user-images.githubusercontent.com/62136051/96272037-28791380-1000-11eb-9a4b-1726e24963c2.png"></p>
