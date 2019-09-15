# Lapres_Modul1_JA1
Lapres_Modul1_JA1

## Capture filter
1.	Filter sehingga wireshark hanya mengambil paket yang mengandung port 21
Jawaban : 

capture filter : port 21
![capture1](https://user-images.githubusercontent.com/42793740/64920332-b755a400-d7e0-11e9-8f0b-a66975ea9f23.png)

2.	Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80 (ajk.if.its.ac.id)

Jawaban :
capture filter : host ajk.if.its.ac.id && src port 80
![capture2](https://user-images.githubusercontent.com/42793740/64920346-e2d88e80-d7e0-11e9-82c5-1667cafbb1b3.png)

3.	Filter sehingga wireshark hanya menampilkan paket yang menuju port 443 (google.com)

Jawaban  :
capture filter : host google.com && dst port 443
![capture3](https://user-images.githubusercontent.com/42793740/64920350-ecfa8d00-d7e0-11e9-9a55-f9f9154cd4a8.png)

4.	Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian

Jawaban :
mencari ip : open command prompt > ipconfig > IPv4 Address
capture filter : ip src 192.168.1.8

![capture4](https://user-images.githubusercontent.com/42793740/64920362-0b608880-d7e1-11e9-886c-9e3c11a6ad4b.png)
![capture4 1](https://user-images.githubusercontent.com/42793740/64920357-f97ee580-d7e0-11e9-8345-bbbaa06add70.png)
 
5.	Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id
Jawaban :
capture filter : dst host monta.if.its.ac.id

![display5 1](https://user-images.githubusercontent.com/42793740/64920377-377c0980-d7e1-11e9-93b7-f563cdf4928e.png)
![display5 2](https://user-images.githubusercontent.com/42793740/64920380-419e0800-d7e1-11e9-915b-7e57995ab534.png)

## Display filter
1.	Tampilkan semua paket yang hostnya mengandung www.ne.its.ac.id

Jawaban:
display filter : http.host == "www.ne.its.ac.id"

![display1](https://user-images.githubusercontent.com/42793740/64920448-1536bb80-d7e2-11e9-8fa7-3800bad12a00.png)

2.	Tampilkan paket yang hanya berasal dari IP 10.151.36 81 dan menuju web "mb.its.ac.id"

Jawaban:
display filter : ip.src == 10.151.36.81 && http.host == "mb.its.ac.id"

![display2](https://user-images.githubusercontent.com/42793740/64920452-254e9b00-d7e2-11e9-985d-1e90c424af3f.png)

Kendala yang dialami :
lupa filter expression yang harus digunakan untuk mencari IP

3.	Simpan gambar ckedokteran.png

Jawaban : File > Export Objects > HTTP… > Text Filter : ckedokteran.png > Save
 
![display3 1](https://user-images.githubusercontent.com/42793740/64920463-47e0b400-d7e2-11e9-9b6f-eef91905b2b6.png)
![display3 2](https://user-images.githubusercontent.com/42793740/64920470-4fa05880-d7e2-11e9-9596-abc2c60992a6.png)
 
Kendala yang dialami : file yang dicari tidak muncul

4.	Cari charset dari halaman "ajk.if.its.ac.id"

Jawaban : 
Display Filter : http == “ajk.if.its.ac.id" > klik kanan salah satu packet >Follow > HTTP stream > find : charset
 
![display4 1](https://user-images.githubusercontent.com/42793740/64920483-69da3680-d7e2-11e9-8060-ba26133d20b9.png)
![display4 2](https://user-images.githubusercontent.com/42793740/64920490-7bbbd980-d7e2-11e9-8e18-a38ac3057166.png)

Kendala yang dialami : tidak ada paket yang memenuhi syarat display filter

5.	Cari username dan password ketika login di "freeshare.lp.if.its ac.id"

Jawaban :
Display Filter : http.request.method == POST && http.host == "freeshare.lp.if.its ac.id" >  Follow > TCP stream > Find : user / Find : password 

![display5 1](https://user-images.githubusercontent.com/42793740/64920495-8a09f580-d7e2-11e9-8e63-b7565d3d27b3.png)
![display5 2](https://user-images.githubusercontent.com/42793740/64920499-955d2100-d7e2-11e9-81dd-7b72036151ed.png)

Kendala yang dialami : tidak ada paket yang memenuhi syarat display filter

6.	Sebutkan web server yang digunakan pada "www.ne.its.ac.id"

http.host == “www.ne.its.ac.id”

![6 1](https://user-images.githubusercontent.com/42793740/64920608-06510880-d7e4-11e9-8cca-8a0caf3df5d4.png)

right click kemudian follow

![6 2](https://user-images.githubusercontent.com/42793740/64920609-06e99f00-d7e4-11e9-83c4-cc19521e68df.png)
	
di kolom find cari “server”
 
![6 3](https://user-images.githubusercontent.com/42793740/64920610-06e99f00-d7e4-11e9-825d-b85fb46f85fa.png)
![6 4](https://user-images.githubusercontent.com/42793740/64920611-06e99f00-d7e4-11e9-9a70-2d1057858f2c.png) 

7.	Sebutkan versi PHP dan yang digunakan pada "riset.ajk.if.its.ac.id"

http.host == "riset.ajk.if.its.ac.id"
 
![7 1](https://user-images.githubusercontent.com/42793740/64920612-07823580-d7e4-11e9-95c5-547b83073709.png)

right click kemudian follow

![7 2](https://user-images.githubusercontent.com/42793740/64920613-07823580-d7e4-11e9-9b97-77904a619f97.png)
	
di kolom find cari “php”
 
![7 3](https://user-images.githubusercontent.com/42793740/64920614-07823580-d7e4-11e9-998a-86acb8492d24.png)
![7 4](https://user-images.githubusercontent.com/42793740/64920615-081acc00-d7e4-11e9-8eec-259a23e53dd9.png) 

8.	Filter pada wireshark kalian sehingga menampilkan hasil ping

icmp

![8](https://user-images.githubusercontent.com/42793740/64920616-081acc00-d7e4-11e9-8862-22fcf3dff2ed.png)

9.	Dapatkan semua metode GET yang mengakses "monta.if.its.ac.id"

http.host == "monta.if.its.ac.id" && http.request.method == GET

![9](https://user-images.githubusercontent.com/42793740/64920617-081acc00-d7e4-11e9-95b7-3d5dbc0c7fe3.png)

10.	Tunjukkan username dan password yang dimasukkan ketika login FTP

ftp.request.command == USER || ftp.request.command == PASS

![10](https://user-images.githubusercontent.com/42793740/64920618-08b36280-d7e4-11e9-8248-54e6d6e3c795.png)

11. 	Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika upload file "qwpeaspojdasjfpasjfpaosuhuy.jpg"

ftp.request.command == STOR && ftp.request.arg == "qwpeaspojdasjfpasjfpaosuhuy.jpg"
 
![11](https://user-images.githubusercontent.com/42793740/64920619-08b36280-d7e4-11e9-9ca6-618874991056.png)

12.	Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika menghapus file "qwpeaspojdasjfpasjfpaos.jpg"

ftp.request.command == DELE && ftp.request.arg == "qwpeaspojdasjfpasjfpaosuhuy.jpg"

![12](https://user-images.githubusercontent.com/42793740/64920620-094bf900-d7e4-11e9-94a2-80a1fcac35fb.png)

13. 	Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika mengganti nama file "sutlin.png"

ftp.request.command == RNFR && ftp.request.arg == "sutlin.png"

![13](https://user-images.githubusercontent.com/42793740/64920621-094bf900-d7e4-11e9-8414-de74ec7b51a2.png)

14.	Tunjukkan di wireshark, paket mana yang dikirimkan FTP client ketika download file "sutlun.png"

ftp.request.command == RETR && ftp.request.arg == "sutlun.png"
 
![14](https://user-images.githubusercontent.com/42793740/64920622-09e48f80-d7e4-11e9-9df0-5e389570efdc.png)
 
 
15.	Cari file .zip di wireshark lalu download dan extract file tersebut clue: "50 4B 03 04"

search di panel find, set menjadi hex value "50 4B 03 04"

![15 1](https://user-images.githubusercontent.com/42793740/64920623-0a7d2600-d7e4-11e9-80a8-35298708563e.png)

pilih salah satu packet, right click kemudian follow

![15 2](https://user-images.githubusercontent.com/42793740/64920624-0a7d2600-d7e4-11e9-84be-3a84bef0656a.png)

right click kemudian follow, pilih TCP stream

![15 3](https://user-images.githubusercontent.com/42793740/64920625-0a7d2600-d7e4-11e9-8ac2-320653bfd8e1.png)

Show and save data as Raw
 
![15 4](https://user-images.githubusercontent.com/42793740/64920627-0b15bc80-d7e4-11e9-9b79-60b5e162fab4.png)

save as hudsafhufaso.zip

![15 5](https://user-images.githubusercontent.com/42793740/64920628-0b15bc80-d7e4-11e9-931e-7c4f8c0664e2.png)

terakhir extract zip tersebut

![15 6](https://user-images.githubusercontent.com/42793740/64920629-0b15bc80-d7e4-11e9-85b9-6e23608bf67a.png)
 
