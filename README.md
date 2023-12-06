# Jarkom-Modul-4-F11-2023
## Kelompok F11
## NAMA :
-	Muhammad Zhafran			(5025211100)
-	Mohamad Valdi Ananda Tauhid		(5025221238)

## Soal :
![SSTopografiSoal](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/b4ce0d70-b616-40fa-8719-d35d3e3f92b9)

## Jawaban
### VLSM
#### Cara Menjawab
1. Bagi topografi menjadi beberapa subnet.
##### Toporafi Pembagian Subnet
![SS Pembagian Daerah Subnet](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/cd4704e2-0cab-4081-8c24-fabea9674db0)

2. Hitung Jumlah IP dari masing-masing subnet dengan cara menjumlahkan total host di dalam subnet.
##### Hasil akhir jumlah IP
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/59e6ab9d-f56b-4d1f-909e-e49c46788e40)

3. Tentukan Netmask dari masing-masing subnet sesuai dengan tabel di bawah:
##### Tabel Netmask
![SS Tabel Netmask ](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/421fd1d1-de56-4cb1-aded-eff74d9f6556)

##### Hasil akhir Netmask Subnet
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/e1248162-7374-4653-b0f7-9482c3f4b3b4)

4. Buat tabel untuk rute.
##### Tabel Rute
![SS Rute Subnet VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/e1248162-7374-4653-b0f7-9482c3f4b3b4)

5. Buat VLSM Tree
##### VLSM Tree
![SS VLSM Tree](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/cfaa3ceb-ad72-4eee-b743-3133180d6342)
![SS VLSM Tree Hasil 1](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/6a1d7f5d-2177-4832-b662-9681cd625571)
![SS VLSM Tree Hasil 2](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/b3ac4aed-a98e-4d9c-aa98-63ea0ed05e07)
![SS VLSM Tree Hasil 3](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/63b14e3e-cc3f-4929-be0d-88140bad5119)
![SS VLSM Tree Hasil 4](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/16a9f834-a454-49ae-8cc5-baefdd0a32aa)
![SS VLSM Tree Hasil 5](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/d254509d-cd99-4614-8620-8d47588fa484)

6. Buat Tabel yang berisi Network ID dari masing-masing subnet sesuai dengan gambar di VLSM Tree lalu isikan juga Netmask dan B Broadcastnya. Ini bisa dihitung dengan cara menambahkan IP dengan wildcard yang nilainya sesuai dengan tabel yang tadi sudah saya tampilkan begitu juga dengan Netmasknya. 
##### Tabel Pembagian IP
![SS Pembagian IP-VLSM](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/bf644da4-9837-4f70-895a-f94bd1ccbc02)

7. Buat Topografi di GNS3
##### Gambar Topografi GNS3
![SS Topografi VLSM GNS3](https://github.com/ZhafranMZ/Jarkom-Modul-2-F11-2023/assets/114043452/efff1c08-5eb1-4597-96a4-89f0d439b3e5)

8. Konfigurasi masing-masing node
##### Konfigurasi masing-masing node
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

### CIDR
#### Cara Menjawab
##### Subnetting dengan metode CIDR
|Kelompok|Network ID|Subnet Mask|
|-|-|-|
|F11|10.57.0.0|/16|

###### Subnet awal
![Frame 1](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/60ee18f3-7f89-4b74-bc4d-7da16a695e74)


|Subnet|Route|Host Amount|Min Subnet Mask|
|-|-|-|-|
|F11-SN1|Aura-Cloud0|2|/30|
|F11-SN2|Aura|2|/30|
|F11-SN3|Aura|2|/30|
|F11-SN4|Aura|2|/30|
|F11-SN5|Aura-Eisen|2|/30|
|F11-SN6|Aura-Eisen|2|/30|
|F11-SN7|Aura-Frieren|2|/30|
|F11-SN8|Aura-Eisen-Linie|2|/30|
|F11-SN9|Aura-Frieren-Flamme|2|/30|
|F11-SN10|Aura-Frieren-Flamme|2|/30|
|F11-SN11|Aura-Denken|127|/24|
|F11-SN12|Aura-Eisen|2|/30|
|F11-SN13|Aura-Eisen|3|/29|
|F11-SN14|Aura-Eisen-Lugner|1001|/22|
|F11-SN15|Aura-Eisen-Lugner|251|/24|
|F11-SN16|Aura-Eisen-Linie|255|/23|
|F11-SN17|Aura-Eisen-Linie-Lawine|31|/26|
|F11-SN18|Aura-Eisen-Linie-Lawine-Switch7-Heiter|512|/22|
|F11-SN19|Aura-Frieren-Flamme-Himmel|6|/29|
|F11-SN20|Aura-Frieren-Flamme|1001|/22|
|F11-SN21|Aura-Frieren-Flamme-Fern|1023|/21|
|F11-SN22|Aura-Frieren|25|/27|


##### Penggabungan-penggabungan yang dilakukan

###### Penggabungan I
![Frame 2](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/ead0c5c0-87f0-45b4-822d-9c751c22b9f3)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(10,21)|F11-SN10|/30|F11-SN21|/21|/20|
|F11-SN(9,19)|F11-SN9|/30|F11-SN19|/29|/28|
|F11-SN(17,18)|F11-SN17|/26|F11-SN18|/22|/21|
|F11-SN(14,15)|F11-SN14|/22|F11-SN15|/22|/21|
|F11-SN(2,11)|F11-SN2|/30|F11-SN11|/24|/23|
|F11-SN(12,13)|F11-SN12|/30|F11-SN13|/29|/28|

###### Penggabungan II
![Frame 3](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/e7a58f64-ac84-4236-86bd-1780783f431a)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(9,19,20)|F11-SN(9,19)|/28|F11-SN20|/22|/21|
|F11-SN(8,17,18)|F11-SN8|/30|F11-SN(17,18)|/21|/20|
|F11-SN(5,14,15)|F11-SN5|/30|F11-SN(14,15)|/21|/20|

###### Penggabungan III
![Frame 4](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/97676778-d37f-46b0-8be8-957fb32597b2)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(9,10,19,20,21)|F11-SN(9,19,20)|/21|F11-SN(10,21)|/20|/19|
|F11-SN(8,16,17,18)|F11-SN(8,17,18)|/20|F11-SN16|/23|/19|
|F11-SN(5,12,13,14,15)|F11-SN(5,14,15)|/20|F11-SN(12,13)|/28|/19|

###### Penggabungan IV
![Frame 5](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/85bf328f-7bef-4f5d-aa55-a779d8d75611)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(7,9,10,19,20,21)|F11-SN7|/30|F11-SN(9,10,19,20,21)|/19|/18|
|F11-SN(6,8,16,17,18)|F11-SN6|/30|F11-SN(8,16,17,18)|/19|/18|

###### Penggabungan V
![Frame 6](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/1ddb74d3-8fe2-42d8-b689-880111cc8c1c)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(5,6,8,12,13,14,15,16,17,18)|F11-SN(6,8,16,17,18)|/18|F11-SN(5,12,13,14,15)|/19|/17|


##### Subnet setelah penggabungan
- F11

![F11-Net](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/fbd6ca7f-364e-4501-a347-3d7b007b6689)

- F11-SN(2,11)

![F11-SN(2,11)](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/37b1eb2a-08d8-407d-8b56-00a204bfa878)

- F11-SN(7,9,10,19,20,21)

![F11-SN(7,9,10,19,20,21)](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/6699ade1-fb01-4d1c-9e91-67b1e47e8003)

- F11-SN(5,6,8,12,13,14,15,16,17,18)

![F11-SN(5,6,8,12,13,14,15,16,17,18)](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/3e1e4fef-1118-4518-934d-47a4a9a44bb7)

- F11-SN(5,12,13,14,15)

![F11-SN(5,12,13,14,15)](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/ee616155-74fd-4257-b372-96a77a0960e3)

- F11-SN(6,8,16,17,18)

![F11-SN(6,8,16,17,18)](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/ba385182-d814-437a-a8a3-9ddf8149725d)

![Frame 6](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/1ddb74d3-8fe2-42d8-b689-880111cc8c1c)

|Subnet|Network ID|CIDR|Subnet Mask|
|-|-|-|-|
|F11SN1|?.?.?.?|/??|
|F11SN2|10.57.2.0|/30|255.255.255.252|
|F11SN3|10.57.0.0|/30|255.255.255.252|
|F11SN4|10.57.0.4|/30|255.255.255.252|
|F11SN5|10.57.208.0|/30|255.255.255.252|
|F11SN6|10.57.128.0|/30|255.255.255.252|
|F11SN7|10.57.64.0|/30|255.255.255.252|
|F11SN8|10.57.160.0|/30|255.255.255.252|
|F11SN9|10.57.122.0|/30|255.255.255.252|
|F11SN10|10.57.96.0|/30|255.255.255.252|
|F11SN11|10.57.3.0|/24|255.255.255.0|
|F11SN12|10.57.192.0|/30|255.255.255.252|
|F11SN13|10.57.192.8|/29|255.255.255.248|
|F11SN14|10.57.216.0|/22|255.255.252.0|
|F11SN15|10.57.220.0|/24|255.255.255.0|
|F11SN16|10.57.176.0|/23|255.255.254.0|
|F11SN17|10.57.168.0|/26|255.255.255.192|
|F11SN18|10.57.172.0|/22|255.255.252.0|
|F11SN19|10.57.112.8|/29|255.255.255.248|
|F11SN20|10.57.116.0|/22|255.255.252.0|
|F11SN21|10.57.104.0|/21|255.255.248.0|
|F11SN22|10.57.0.32|/27|255.255.255.224|
|F11-SN(10,21)|10.57.96/0|/20|255.255.240.0|
|F11-SN(9,19)|10.57.112.0|/28|255.255.255.240|
|F11-SN(17,18)|10.57.168.0|/21|255.255.248.0|
|F11-SN(14,15)|10.57.216.0|/21|255.255.248.0|
|F11-SN(2,11)|10.57.2.0|/23|255.255.254.0|
|F11-SN(12,13)|10.57.192.0|/28|255.255.255.240|
|F11-SN(9,19,20)|10.57.112.0|/21|255.255.248.0|
|F11-SN(8,17,18)|10.57.160.0|/20|255.255.240.0|
|F11-SN(5,14,15)|10.57.208.0|/20|255.255.240.0|
|F11-SN(9,10,19,20,21)|10.57.96.0|/19|255.255.224.0|
|F11-SN(8,16,17,18)|10.57.160.0|/19|255.255.224.0|
|F11-SN(5,12,13,14,15)|10.57.192.0|/19|255.255.224.0|
|F11-SN(7,9,10,19,20,21)|10.57.64.0|/18|255.255.192.0|
|F11-SN(6,8,16,17,18)|10.57.128.0|/18|255.255.192.0|
|F11-SN(5,6,8,12,13,14,15,16,17,18)|10.57.128.0|/17|255.255.128.0|

##### Routing Table

###### Aura
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|10.57.2.0|/23|10.57.2.2|
|10.57.128.0|/17|10.57.0.2|
|10.57.0.32|/27|10.57.0.6|
|10.57.64.0|/18|10.57.0.6|

###### Denken
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.2.1|

###### Eisen
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.0.1|
|10.57.216.0|/21|10.57.208.2|
|10.57.128.0|/18|10.57.128.2|

###### Lugner
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.208.1|

###### Linie
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.128.1|
|10.57.168.0|/21|10.57.160.2|

###### Lawine
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.160.1|
|10.57.172.0|/22|10.57.168.2|

###### Heiter
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.168.1|

###### Frieren
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.0.5|
|10.57.64.0|/18|10.57.64.2|
|10.57.0.32|/27|10.57.0.34|

###### Flamme
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.64.1|
|10.57.112.8|/29|10.57.122.2|
|10.57.104.0|/21|10.57.96.2|

###### Himmel
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.122.1|

###### Fern
|Network ID|Subnet Mask|Next Hop|
|-|-|-|
|0.0.0.0|/0|10.57.96.1|
