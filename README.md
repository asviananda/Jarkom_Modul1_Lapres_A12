# Jarkom_Modul1_Lapres_A12

- Achmad Sofyan Pratama (05111840000061)
- Oktarizka Asviananda Nursanty (05111840000156)


**A. DISPLAY FILTER**

**1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!**

Menggunakan ```http.host contains "testing.mekanis.me"``` kemudian keluar paket-paket berikut :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96338396-fcb96480-10b7-11eb-9e53-9d7a0baead3e.png"></p>

Kemudian, pilih salah satu paket, klik kanan paket tersebut, lalu klik ```Follow``` dilanjut ```HTTP stream``` didapat hasil sbg berikut :
<p align = "center"><img width = "500" src="https://user-images.githubusercontent.com/62512432/96338559-3a6abd00-10b9-11eb-849d-653d78f8511f.png"></p>

Terdapat keterangan pada gambar diatas bahwa webserver yang digunakan pada "testing.mekanis.me" adalah ```Server : nginx/1.14.0 (Ubuntu)```

**2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!**

**Cara 1** : Menggunakan ```http contains Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg``` kemudian keluar paket berikut :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96338763-73576180-10ba-11eb-899e-1f1c72114d39.png"></p>

Kemudian klik paket yang ada, kemudian akan muncul gambar berikut :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96338860-02fd1000-10bb-11eb-8cf2-9663274ed0c9.png"></p>

Lalu klik link ```[Full request URI: http://www.dpr.go.id/dokpemberitaan/news-photo/Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg]```, lalu akan muncul gambar yang diminta, kemudian klik kanan gambar tersebut lalu klik ```Save image as...``` dan simpan gambar tsb seperti menyimpan gambar pada umumnya.

**Cara 2** : Setelah muncul paket, klik ```File``` , pilih ```Export object```, lalu pilih ```HTTP```, kemudian kita filter lagi dibagian ```Text filter``` dengan ```Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg``` agar keluar gambar yang diminta saja seperti gambar dibawah :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96339440-e95dc780-10be-11eb-8a19-ee7359153cba.png"></p>

lalu klik paket tsb kemudian klik save untuk menyimpan gambar. Berikut ini adalah gambar yang diminta :
<p align ="center"><img width ="500" src ="https://user-images.githubusercontent.com/62512432/96339493-48234100-10bf-11eb-8063-e81b483d742d.png"></p>

**3. Cari username dan password ketika login di "ppid.dpr.go.id"!**

Menggunakan ```http.request.method == POST``` kemudian muncul paket sbg berikut :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96339805-07c4c280-10c1-11eb-82a5-8102cc98591f.png"></p>

kemudian apabila paket tersebut diklik, akan muncul username dan password yang diminta pada bagian ```HTML Form URL Encoded```
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96339701-9258f200-10c0-11eb-99cf-4dfca1d97723.png"></p>

pada gambar tersebut, diketahui bahwa ```username : 10pemuda``` dan ```password: guncangdunia```

**4. Temukan paket dari web-web yang menggunakan basic authentication method!**

Menggunakan ```http.authbasic``` untuk menemukan paket dari web-web yang menggunakan basic authentication method. Didapatkan paket-paket tsb sbg berikut :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96339866-625e1e80-10c1-11eb-87f8-ae77cfec87b9.png"></p>

**5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!**

Menggunakan ```ip.dst == 157.245.50.224 && http``` untuk mencari username dan password agar dapat mengakses web "aku.pengen.pw". Akan muncul paket-paket yang menuju ip tersebut :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96339973-30998780-10c2-11eb-948d-de7609b51c45.png"></p>


lalu klik salah satu paket yang mengandung ```Authorization: Basic``` , karena web "aku.pengen.pw" merupakan basic authentication. Akan ditemukan pada bagian ```credentials``` yang berisikan ```username : kakakgamtenk``` dan ```password : hartatahtabermuda``` seperti gambar dibawah :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96340840-1f9d4600-10c3-11eb-8b88-63eb4a16e5a8.png"></p>

setelah berhasil login web, didapatkan isi dari laman web tsb sbg berikut :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96342277-b79b2f80-10c3-11eb-8fe3-b5dd66d2c0b9.png"></p>

**6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).**

Menggunakan ```ftp-data + (CTRL+F)``` untuk mencari file "Answer.zip"
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96343278-0ea10480-10c4-11eb-8e06-ab459c8eb1ed.png"></p>

lalu sehabis itu klik kanan, pilih ```Follow``` kemudian ```TCP stream```, ubah dahulu isinya dari bentuk ASCII menjadi bentuk raw. Kemudian, save isi paket tsb. Untuk mendapatkan isi dari file "zipkey.txt", gunakan ```zipkey.txt``` pada kotak find, lalu pilih salah satu paket, klik kanan, pilih ```Follow``` dan ```TCP stream```. Didapatkan hasil dari "zipkey.txt" adalah :
<p align="center"><img width ="200" src="https://user-images.githubusercontent.com/62512432/96346729-8b81ad80-10c7-11eb-9c93-4ffe27ef5124.png"></p>

setelah mendapat password, file "Answer.zip" diekstrak dan buka file "Open This.pdf". Masukkan password yang sudah ditemukan, kemudian didapat gambar :
<p align="center"><img width ="500" src="https://user-images.githubusercontent.com/62512432/96346885-69d4f600-10c8-11eb-88a8-8202e5ab0b53.png"></p>

**7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"**

**8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!**

Cari paket yang berasal dari koneksi FTP dengan Microsoft FTP Service menggunakan ```ftp contains "Microsoft"``` kemudian akan keluar hasil spt ini :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96358833-c9b5b600-1135-11eb-9e3d-a8443d2542b7.png"></p>

kemudian pilih ip Microsoft FTP Service untuk mencari objek apa yang didownload menggunakan ```RETR``` , akan keluar hasil :
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96358811-a2f77f80-1135-11eb-82de-fbfe7fb65071.png"></p>


**9. Cari username dan password ketika login FTP pada localhost!**

Menggunakan ```ftp&&ftp.command == USER || ftp.request.command == PASS```
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96347202-5aef4300-10ca-11eb-868f-f4180098b66d.png"></p>

display capture ```ftp``` digunakan karena protokol yang digunakan adalah FTP. Dan karena diminta username dan password, maka digunakan display capture ```ftp.command == USER || ftp.request.command == PASS```. Didapatlah hasil sesuai dengan gambar diatas.

**10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46"**

Pertama, terdapat clue "25 50 44 46" yang merupakan ```hex value``` yang dapat dicari dengan ```CTRL+F``` search ```hex value 25 50 44 46```
<p align="center"><img src="https://user-images.githubusercontent.com/62512432/96347700-a48d5d00-10cd-11eb-92e6-9dbd85d4eed5.png"></p>

kemudian pilih salah satu paket, klik kanan, pilih ```Follow``` kemudian pilih ```TCP stream```, ubah menjadi raw kemudian save as pdf. Apabila file pdf tersebut dibuka, maka akan berisi :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96358034-06c97a80-112d-11eb-8ec6-b6e27742d3bb.png"></p>


**B. CAPTURE FILTER**

**11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!**

**12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!**

**13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!**

**14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!**

Cari ip laptop menggunakan command prompt dengan ```ipconfig```, didapat hasilnya :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96358087-8f481b00-112d-11eb-904b-623071d821a3.png"></p>

lalu gunakan ```ip.src == 192.168.100.40```, didapatkan hasil sbg berikut :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96358127-ee0d9480-112d-11eb-84bc-dd79479a2dc4.png"></p>

**15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!**

Cari ip monta.if.its.ac.id menggunakan command prompt dengan ```ping monta.if.its.ac.id```, didapat hasilnya :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96358163-375de400-112e-11eb-9b05-0a9226912a4c.png"></p>

lalu gunakan ```ip.dst == 103.94.190.11```, didapatkan hasil sbg berikut :
<p align ="center"><img src="https://user-images.githubusercontent.com/62512432/96358196-a8050080-112e-11eb-9f36-bd6f2c7e7475.png"></p>
