# Subnetting dengan metode CIDR
|Kelompok|Network ID|Subnet Mask|
|-|-|-|
|F11|10.57.0.0|/16|

## List subnet awal
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
## Pengelompokan yang dilakukan


## List subnet akhir
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


|Subnet|Network ID|Subnet Mask|CIDR|Broadcast|
|-|-|-|-|-|
|F11-SN(5,6,8,12,13,14,15,16,17,18)|10.57.128.0|255.255.128.0|/17|10.57.255.255|
|F11-SN(7,9,10,19,20,21)|10.57.64.0|255.255.192.0|/18|10.57.127.255|
|F11-SN(2,11)|10.57.2.0|255.255.254.0|/23|10.57.3.255|
|F11-SN22|10.57.0.32|255.255.255.224|/27|10.57.0.63|
|F11-SN4|10.57.0.4|255.255.255.252|/30|10.57.0.7|
|F11-SN3|10.57.0.0|255.255.255.252|/30|10.57.0.3|
