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
