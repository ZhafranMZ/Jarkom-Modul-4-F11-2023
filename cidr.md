# Subnetting dengan metode CIDR
|Kelompok|Network ID|Subnet Mask|
|-|-|-|
|F11|10.57.0.0|/16|

## Subnet awal
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


## Penggabungan-penggabungan yang dilakukan

### Penggabungan I
![Frame 2](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/ead0c5c0-87f0-45b4-822d-9c751c22b9f3)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(10,21)|F11-SN10|/30|F11-SN21|/21|/20|
|F11-SN(9,19)|F11-SN9|/30|F11-SN19|/29|/28|
|F11-SN(17,18)|F11-SN17|/26|F11-SN18|/22|/21|
|F11-SN(14,15)|F11-SN14|/22|F11-SN15|/22|/21|
|F11-SN(2,11)|F11-SN2|/30|F11-SN11|/24|/23|
|F11-SN(12,13)|F11-SN12|/30|F11-SN13|/29|/28|

### Penggabungan II
![Frame 3](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/e7a58f64-ac84-4236-86bd-1780783f431a)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(9,19,20)|F11-SN(9,19)|/28|F11-SN20|/22|/21|
|F11-SN(8,17,18)|F11-SN8|/30|F11-SN(17,18)|/21|/20|
|F11-SN(5,14,15)|F11-SN5|/30|F11-SN(14,15)|/21|/20|

### Penggabungan III
![Frame 4](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/97676778-d37f-46b0-8be8-957fb32597b2)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(9,10,19,20,21)|F11-SN(9,19,20)|/21|F11-SN(10,21)|/20|/19|
|F11-SN(8,16,17,18)|F11-SN(8,17,18)|/20|F11-SN16|/23|/19|
|F11-SN(5,12,13,14,15)|F11-SN(5,14,15)|/20|F11-SN(12,13)|/28|/19|

### Penggabungan IV
![Frame 5](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/85bf328f-7bef-4f5d-aa55-a779d8d75611)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(7,9,10,19,20,21)|F11-SN7|/30|F11-SN(9,10,19,20,21)|/19|/18|
|F11-SN(6,8,16,17,18)|F11-SN6|/30|F11-SN(8,16,17,18)|/19|/18|

### Penggabungan V
![Frame 6](https://github.com/ZhafranMZ/Jarkom-Modul-4-F11-2023/assets/63389207/1ddb74d3-8fe2-42d8-b689-880111cc8c1c)
|Subnet Akhir|Subnet A|Subnet Mask A|Subnet B|Subnet Mask B|Subnet Mask Akhir|
|-|-|-|-|-|-|
|F11-SN(5,6,8,12,13,14,15,16,17,18)|F11-SN(6,8,16,17,18)|/18|F11-SN(5,12,13,14,15)|/19|/17|


## Subnet setelah penggabungan
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
