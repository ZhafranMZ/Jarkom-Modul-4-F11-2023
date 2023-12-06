# Jarkom-Modul-4-F11-2023
## Kelompok F11
## NAMA :
-	Muhammad Zhafran			(5025211100)
-	Mohamad Valdi Ananda Tauhid		(5025221238)

## Soal :
Gambar Toporafi:
![SSTopografiSoal](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/b4ce0d70-b616-40fa-8719-d35d3e3f92b9)

## Jawaban
### VLSM
#### Cara Menjawab
1. Bagi topografi menjadi beberapa subnet.
##### Toporafi Pembagian Subnet
Gambar:
![SS Pembagian Daerah Subnet](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/cd4704e2-0cab-4081-8c24-fabea9674db0)

2. Hitung Jumlah IP dari masing-masing subnet dengan cara menjumlahkan total host di dalam subnet.
##### Hasil akhir jumlah IP
Gambar:
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/59e6ab9d-f56b-4d1f-909e-e49c46788e40)

3. Tentukan Netmask dari masing-masing subnet sesuai dengan tabel di bawah:
##### Tabel Netmask
Gambar:
![SS Tabel Netmask ](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/421fd1d1-de56-4cb1-aded-eff74d9f6556)

##### Hasil akhir Netmask Subnet
Gambar:
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/e1248162-7374-4653-b0f7-9482c3f4b3b4)

4. Buat tabel untuk rute.
##### Tabel Rute
Gambar:
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/e1248162-7374-4653-b0f7-9482c3f4b3b4)

5. Buat VLSM Tree
##### VLSM Tree
Gambar:
![SS VLSM Tree](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/cfaa3ceb-ad72-4eee-b743-3133180d6342)
![SS VLSM Tree Hasil 1](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/6a1d7f5d-2177-4832-b662-9681cd625571)
![SS VLSM Tree Hasil 2](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/b3ac4aed-a98e-4d9c-aa98-63ea0ed05e07)
![SS VLSM Tree Hasil 3](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/63b14e3e-cc3f-4929-be0d-88140bad5119)
![SS VLSM Tree Hasil 4](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/16a9f834-a454-49ae-8cc5-baefdd0a32aa)
![SS VLSM Tree Hasil 5](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/d254509d-cd99-4614-8620-8d47588fa484)

6. Buat Tabel yang berisi Network ID dari masing-masing subnet sesuai dengan gambar di VLSM Tree lalu isikan juga Netmask dan B Broadcastnya. Ini bisa dihitung dengan cara menambahkan IP dengan wildcard yang nilainya sesuai dengan tabel yang tadi sudah saya tampilkan begitu juga dengan Netmasknya. 
##### Tabel Pembagian IP
Gambar:
![SS Pembagian IP-VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/bf644da4-9837-4f70-895a-f94bd1ccbc02)

7. Buat Topografi di GNS3
##### Gambar Topografi GNS3
Gambar:
![SS Topografi VLSM GNS3](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/efff1c08-5eb1-4597-96a4-89f0d439b3e5)

8. Konfigurasi masing-masing node
##### Konfigurasi masing-masing node
Kode:
```
#Aura
#a1 - 0
auto eth0
iface eth0 inet dhcp
	adress 10.57.1.1
	netmask 255.255.255.252
#a2 - 1
auto eth1
iface eth1 inet static
        address 10.57.1.5
        netmask 255.255.255.252
#a3 - 2
auto eth2
iface eth2 inet static
         address 10.57.1.9
         netmask 255.255.255.252
#a4 - 3
auto eth3
iface eth3 inet static
         address 10.57.1.13
         netmask 255.255.255.252

******
#Frieren
#a4 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.14
          netmask 255.255.255.252
          gateway 10.57.1.13
#a7 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.25
          netmask 255.255.255.252
#a22 - 2
auto eth2
iface eth2 inet static
          address 10.57.1.65
          netmask 255.255.255.224

******
#LakeKorridor
#a22 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.66
          netmask 255.255.255.224
          gateway 10.57.1.65

******
#Flamme
#a7 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.26
          netmask 255.255.255.252
          gateway 10.57.1.25
#a9 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.33
          netmask 255.255.255.252
#a10 - 2
auto eth2
iface eth2 inet static
          address 10.57.1.37
          netmask 255.255.255.252
#a20 - 3
auto eth3
iface eth2 inet static
          address 10.57.17.1
          netmask 255.255.252.0

******
#Himmel
#a9 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.34
          netmask 255.255.255.252
          gateway 10.57.1.33
#a19 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.57
          netmask 255.255.255.248

******
#SchwerMountains
#a19 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.58
          netmask 255.255.255.248
          gateway 10.57.1.57

******
#Fern
#a10 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.38
          netmask 255.255.255.252
          gateway 10.57.1.37
#a21 - 1
auto eth1
iface eth1 inet static
          address 10.57.25.1
          netmask 255.255.248.0

*******
#LaubHills
#a21 - 0
auto eth0
iface eth0 inet static
          address 10.57.25.2
          netmask 255.255.248.0
          gateway 10.57.25.1

*******
#AppetitRegion
#a21 - 0
auto eth0
iface eth0 inet static
          address 10.57.25.3
          netmask 255.255.248.0
          gateway 10.57.25.1

*******
#RohrRoad
#a20 - 0
auto eth0
iface eth0 inet static
          address 10.57.17.2
          netmask 255.255.252.0
          gateway 10.57.17.1

******
#Denken
#a2 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.6
          netmask 255.255.255.252
          gateway 10.57.1.5
#a11 - 1
auto eth1
iface eth1 inet static
          address 10.57.2.1
          netmask 255.255.255.0

*******
#RoyalCapital
#a11 - 0
auto eth0
iface eth0 inet static
          address 10.57.2.2
          netmask 255.255.255.0
          gateway 10.57.2.1

*******
#WilleRegion
#a11 - 0
auto eth0
iface eth0 inet static
          address 10.57.2.3
          netmask 255.255.255.0
          gateway 10.57.2.1

*******
#Eisen
#a3 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.10
          netmask 255.255.255.252
          gateway 10.57.1.9
#a5 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.17
          netmask 255.255.255.252
#a6 - 2
auto eth2
iface eth2 inet static
          address 10.57.1.21
          netmask 255.255.255.252
#a12 - 3
auto eth3
iface eth3 inet static
          address 10.57.1.41
          netmask 255.255.255.252
#a13 - 4
auto eth4
iface eth4 inet static
          address 10.57.1.49
          netmask 255.255.255.248

*******
#Richter
#a13 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.50
          netmask 255.255.255.248
          gateway 10.57.1.49

*******
#Revolte
#a13 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.51
          netmask 255.255.255.248
          gateway 10.57.1.49

*******
#Stark
#a12 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.42
          netmask 255.255.255.252
          gateway 10.57.1.41

*******
#Lugner
#a5 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.18
          netmask 255.255.255.252
          gateway 10.57.1.17
#a14 - 1
auto eth1
iface eth1 inet static
          address 10.57.9.1
          netmask 255.255.252.0
#a15 - 2
auto eth2
iface eth2 inet static
          address 10.57.3.1
          netmask 255.255.255.0

*******
#TurkRegion
#a14 - 0
auto eth0
iface eth0 inet static
          address 10.57.9.2
          netmask 255.255.252.0
          gateway 10.57.9.1

*******
#GrobeForest
#a15 - 0
auto eth0
iface eth0 inet static
          address 10.57.3.2
          netmask 255.255.255.0
          gateway 10.57.3.1

******
#Linie
#a6 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.22
          netmask 255.255.255.252
          gateway 10.57.1.21
#a8 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.29
          netmask 255.255.255.252
#a16 - 2
auto eth2
iface eth2 inet static
          address 10.57.5.1
          netmask 255.255.254.0

******
#GranzChannel
#a6 - 0
auto eth0
iface eth0 inet static
          address 10.57.5.2
          netmask 255.255.254.0
          gateway 10.57.5.1

******
#Lawine
#a8 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.30
          netmask 255.255.255.252
          gateway 10.57.1.29
#a17 - 1
auto eth1
iface eth1 inet static
          address 10.57.1.129
          netmask 255.255.255.192

******
#BredtRegion
#a17 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.130
          netmask 255.255.255.192
          gateway 10.57.1.129

******
#Heiter
#a17 - 0
auto eth0
iface eth0 inet static
          address 10.57.1.131
          netmask 255.255.255.192
          gateway 10.57.1.129
#a18 - 1
auto eth1
iface eth1 inet static
          address 10.57.13.1
          netmask 255.255.252.0

******
#RiegelCanyon
#a18 - 0
auto eth0
iface eth0 inet static
          address 10.57.13.2
          netmask 255.255.252.0
          gateway 10.57.13.1

******
#Sein
#a18 - 0
auto eth0
iface eth0 inet static
          address 10.57.13.3
          netmask 255.255.252.0
          gateway 10.57.13.1
```

9. Ping masing-masing node di command
##### SS ping masing-masing node
Gambar:
![AppetitRegion](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/a8c671b6-4557-4792-8148-83452c516f41)
![Aura](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/b5689300-052e-4a6c-95fa-e3d596bccdec)
![BredtRegion](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/3d22160d-84df-4d54-b913-685cd3a031a9)
![Denken](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/9c018343-3856-4b93-8e56-9f1587e41171)
![Eisen](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/bc1b9e3d-b538-4470-a2cb-c8a362143ed2)
![Fern](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/426fcce0-33b0-4973-a023-2d9c86807d5e)
![RohrRoad](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/8cd26cc2-b319-4b61-98f2-9419d915266a)
![RoyalCapital](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/a5915bb2-892f-4882-8ffd-1ca372916c7f)
![SchwerMountains](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/5e2a27c1-3c9d-4aa9-b3d4-ba057d504ba8)
![Sein](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/686f81df-8523-44d9-91d3-f737bfb89817)
![Stark](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/5a017c16-4365-4393-9170-f0c18a832283)
![TurkRegion](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/c1e57e07-aa53-40ad-a64c-06547600102d)
![WilleRegion](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/591ada00-4f32-4291-a348-d57c3dbc72cd)
![Flamme](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/5708840f-087a-409b-9ea0-16a4a773767b)
![Frieren](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/2f0e8ec6-e0d3-4f88-a6a0-0e4f58759900)
![GranzChannel](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/58d6b344-b67b-4e66-9dee-442548529d86)
![GrobeForest](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/3973c834-9566-4bba-a557-a9b949f18145)
![Heiter](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/bf7aaf29-874b-4fff-910c-5588928e9214)
![Himmel](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/e6114737-1576-454a-b6db-7037c91e42a9)
![LakeKorridor](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/48ec10e1-0a48-41ee-b672-2623bb8b2066)
![LaubHills](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/8f26695d-06c5-4e61-9b2f-11deb0754081)
![Lawine](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/00489568-8315-4561-8db6-2a42a7005483)
![Linie](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/d23a018d-bba4-4255-9ae7-55ab7d97c7ca)
![Lugner](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/2a330b5b-a9e7-4c08-9d95-0b8b2f5ed08f)
![Revolte](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/232645a0-f833-4270-963b-a07ee720c162)
![Richter](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/2fdcd8ba-a89f-4ad4-9ac8-bd017dbe1f43)
![RiegelCanyon](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/18726e4b-1f44-4d1a-aefb-fbc739a80273)
