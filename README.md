# Jarkom-Modul-4-T11-2021


Nama Anggota | NRP
------------------- | --------------		
Justin Alfonsius Sitanggang | 05311840000043
Daniel Evan | 05311940000016
Calvin Manuel | 05311940000049


## SOAL

### VLSM
Berikut adalah pembagian yang kami lakukan dari topologi yang ada pada CPT



### CIDR
#### Pembagian Subnet
Berikut adalah pembagian yang kami lakukan dari topologi yang ada
<br><br>
<img src="/cidr/T11_Pembagian Subnet CIDR.jpg">
<br><br>
Terdapat total 14 lingkaran yang menggabungkan subnet-subnet yang telah ada, dengan pembagian sebagai berikut
<br><br>
<img src="/cidr/CIDR_excel.JPG">
### Tree
Dari perhitungan subnet tersebut selanjutnya kami membuat tree yang berisi pembagian IP ke setiap node yang ada, berikut adalah tree yang kami buat.
<br><br>
<img src="/cidr/T11_tree cidr.jpg">
<br><br>
Dikarenakan kami mendapat prefix 10.47 sedangkan pada netmask /15 tidak ada 10.47 maka perlu kami turunkan hingga /17 untuk mendapatkan prefix IP kami.
### Konfigurasi
#### Membuat Topologi di GNS3
Selanjutnya kami membuat topologi tersebut pada GNS3, seperti gambar berikut ini.
<br><br>
<img src="/cidr/cidr gns.JPG">
<br><br>
#### Pengaturan Interface dan IP pada tiap node
Foosha
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.47.12.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.47.0.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.47.0.17
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.47.0.21
	netmask 255.255.255.252
```
Blueno
```
auto eth0
iface eth0 inet static
	address 10.47.12.2
	netmask 255.255.252.0
        gateway 10.47.12.1
```
Water7
```
auto eth0
iface eth0 inet static
	address 10.47.0.2
	netmask 255.255.255.252
        gateway 10.47.0.1

auto eth1
iface eth1 inet static
	address 10.47.8.1
	netmask 255.255.252.0
        gateway 10.47.0.1

auto eth2
iface eth2 inet static
	address 10.47.0.5
	netmask 255.255.255.252
        gateway 10.47.0.1
```
Cipher
```
auto eth0
iface eth0 inet static
	address 10.47.8.2
	netmask 255.255.252.0
        gateway 10.47.8.1
```
Pucci
```
auto eth0
iface eth0 inet static
	address 10.47.0.6
	netmask 255.255.255.252
        gateway 10.47.0.5

auto eth1
iface eth1 inet static
	address 10.47.1.129
	netmask 255.255.255.128
        gateway 10.47.0.5

auto eth2
iface eth2 inet static
	address 10.47.24.1
	netmask 255.255.248.0
        gateway 10.47.0.5
```
Jipangu
```
auto eth0
iface eth0 inet static
	address 10.47.1.130
	netmask 255.255.255.128
        gateway 10.47.1.129
```
Courtyard
```
auto eth0
iface eth0 inet static
	address 10.47.24.2
	netmask 255.255.248.0
        gateway 10.47.24.1
```
Calmbelt
```
auto eth0
iface eth0 inet static
	address 10.47.24.3
	netmask 255.255.248.0
        gateway 10.47.24.1
```
Doriki
```
auto eth0
iface eth0 inet static
	address 10.47.0.18
	netmask 255.255.255.252
        gateway 10.47.0.17
```
Guanhao
```
auto eth0
iface eth0 inet static
	address 10.47.0.22
	netmask 255.255.255.252
	gateway 10.47.0.21

auto eth1
iface eth1 inet static
	address 10.47.16.1
	netmask 255.255.252.0
	gateway 10.47.0.21

auto eth2
iface eth2 inet static
	address 10.47.0.129
	netmask 255.255.255.252
	gateway 10.47.0.21

auto eth3
iface eth3 inet static
	address 10.47.4.1
	netmask 255.255.254.0
	gateway 10.47.0.21
```
Jabra
```
auto eth0
iface eth0 inet static
	address 10.47.16.2
	netmask 255.255.252.0
	gateway 10.47.16.1
```
Maingate
```
auto eth0
iface eth0 inet static
	address 10.47.4.2
	netmask 255.255.254.0
	gateway 10.47.4.1
```
Alabasta
```
auto eth0
iface eth0 inet static
	address 10.47.4.3
	netmask 255.255.254.0
	gateway 10.47.4.1

auto eth1
iface eth1 inet static
	address 10.47.1.1
	netmask 255.255.255.240
	gateway 10.47.4.1
```
Jorge
```
auto eth0
iface eth0 inet static
	address 10.47.1.2
	netmask 255.255.255.240
	gateway 10.47.1.1
```
OIMO
```
auto eth0
iface eth0 inet static
	address 10.47.0.130
	netmask 255.255.255.252
	gateway 10.47.0.129

auto eth1
iface eth1 inet static
	address 10.47.2.1
	netmask 255.255.255.0
	gateway 10.47.0.129

auto eth2
iface eth2 inet static
	address 10.47.0.133
	netmask 255.255.255.252
	gateway 10.47.0.129
```
EniesLobby
```
auto eth0
iface eth0 inet static
	address 10.47.2.2
	netmask 255.255.255.0
	gateway 10.47.2.1
```
Seastone
```
auto eth0
iface eth0 inet static
	address 10.47.2.3
	netmask 255.255.255.0
	gateway 10.47.2.1

auto eth1
iface eth1 inet static
	address 10.47.20.1
	netmask 255.255.252.0
	gateway 10.47.2.1
```
Elena
```
auto eth0
iface eth0 inet static
	address 10.47.20.2
	netmask 255.255.252.0
	gateway 10.47.20.1
```
Fukurou
```
auto eth0
iface eth0 inet static
	address 10.47.0.134
	netmask 255.255.255.252
	gateway 10.47.0.133
```
#### Routing
Foosha
```
route add -net 10.47.8.0 netmask 255.255.252.0 gw 10.47.0.2
route add -net 10.47.1.128 netmask 255.255.255.128 gw 10.47.0.2
route add -net 10.47.24.0 netmask 255.255.248.0 gw 10.47.0.2
route add -net 10.47.16.0 netmask 255.255.252.0 gw 10.47.0.22
route add -net 10.47.1.0 netmask 255.255.255.240 gw 10.47.0.22
route add -net 10.47.0.132 netmask 255.255.255.252 gw 10.47.0.22
route add -net 10.47.2.0 netmask 255.255.255.0 gw 10.47.0.22
route add -net 10.47.20.0 netmask 255.255.252.0 gw 10.47.0.22
route add -net 10.47.4.0 netmask 255.255.254.0 gw 10.47.0.22
route add -net 10.47.0.4 netmask 255.255.255.252 gw 10.47.0.2
route add -net 10.47.0.128 netmask 255.255.255.252 gw 10.47.0.22
```
Water7
```
route add -net 10.47.1.128 netmask 255.255.255.128 gw 10.47.0.6
route add -net 10.47.24.0 netmask 255.255.248.0 gw 10.47.0.6
```
Guanhao
```
route add -net 10.47.1.0 netmask 255.255.255.240 gw 10.47.4.3
route add -net 10.47.0.132 netmask 255.255.255.252 gw 10.47.0.130
route add -net 10.47.2.0 netmask 255.255.255.0 gw 10.47.0.130
route add -net 10.47.20.0 netmask 255.255.252.0 gw 10.47.0.130
```
OIMO
```
route add -net 10.47.20.0 netmask 255.255.252.0 gw 10.47.2.3
```

### Kendala
1. Pada awalnya kami merasa kesulitan dalam membuat tree dan pembagian CIDR, setelah membaca-baca kembali modul akhirnya kami bisa membuat tree dan pembagian CIDR
2. Untuk routing terkadang ada beberapa IP yang terlewat, sehingga perlu lebih teliti.
