# jarkom-modul-5-C14-2021

Praktikum Jaringan Komputer Modul 5 
### Nama Anggota Kelompok:
1. 05111940000059 	Dido Fabian Fayed <br>
2. 05111940000074	Nur Ahmad Khatim <br>
3. 05111940000162	Ramadhan Arif Hardijansyah <br>

## VLSM
### Subnetting
1. Melakukan subnetting pada topologi yang diberikan. Sehingga terbentuk 8 subnet
![VLSM](img/VLSM_1_Subnetting.png)

2. Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melakukan labelling netmask berdasarkan jumlah IP yang dibutuhkan. <br>
![VLSM](img/VLSM_2_JumlahIP.png) <br>
Berdasarkan total IP dan netmask yang dibutuhkan, maka dapat menggunakan netmask /21 untuk memberikan pengalamatan IP pada subnet.

3. Subnet besar yang dibentuk memiliki NID 10.21.0.0 dengan netmask /21. Selanjutnya menghitung pembagian IP berdasarkan NID dan netmask tersebut menggunakan pohon seperti gambar berikut. <br>
![VLSM](img/VLSM_3_Tree.png) <br>
![VLSM](img/VLSM_4_Table.png) <br>

### A. Topologi <br>
![VLSM](img/VLSM_5_Topology.png) <br>

### B. Konfigurasi IP setiap interface sesuai pembagian subnet pada tree

#### Foosha
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp
        address 10.21.0.10
       netmask 255.255.255.252
       gateway 10.21.0.9

auto eth1
iface eth1 inet static
        address 10.21.0.1
        netmask 255.255.255.252

auto eth2
iface eth2 inet static
         address 10.21.0.5
         netmask 255.255.255.252
```

#### Water7
```
auto eth0
iface eth0 inet static
        address 10.21.0.2
        netmask 255.255.255.252
        gateway 10.21.0.1

auto eth1
iface eth1 inet static
        address 10.21.0.17
        netmask 255.255.255.248

auto eth2
iface eth2 inet static
         address 10.21.0.129
         netmask 255.255.255.128

auto eth3
iface eth3 inet static
         address 10.21.4.1
         netmask 255.255.252.0
```

#### Guanhao
```
auto eth0
iface eth0 inet static
          address 10.21.0.6
          netmask 255.255.255.252
          gateway 10.21.0.5

auto eth1
iface eth1 inet static
          address 10.21.0.25
          netmask 255.255.255.248

auto eth2
iface eth2 inet static
          address 10.21.1.1
          netmask 255.255.255.0

auto eth3
iface eth3 inet static
           address 10.21.2.1
          netmask 255.255.254.0
```

#### Blueno
```
#auto eth0
#iface eth0 inet static
 #      address 10.21.0.130
 #      netmask 255.255.255.128
  #     gateway 10.21.0.129

auto eth0
iface eth0 inet dhcp
```

#### Chiper
```
#auto eth0
#iface eth0 inet static
#       address 10.21.4.2
#      netmask 255.255.252.0
#       gateway 10.21.4.1

auto eth0
iface eth0 inet dhcp
```

#### Elena
```
auto eth0
iface eth0 inet static
       address 10.21.2.2
       netmask 255.255.254.0
       gateway 10.21.2.1

#auto eth0
#iface eth0 inet dhcp
```

#### Fukurou
```
#auto eth0
#iface eth0 inet static
#       address 10.21.1.2
#       netmask 255.255.255.0
#       gateway 10.21.1.1

auto eth0
iface eth0 inet dhcp
```

#### Maingate
```
auto eth0
iface eth0 inet static
       address 10.21.0.27
       netmask 255.255.255.248
       gateway 10.21.0.25
```

#### Jorge
```
auto eth0
iface eth0 inet static
       address 10.21.0.26
       netmask 255.255.255.248
       gateway 10.21.0.25
```

#### Doriki
```
auto eth0
iface eth0 inet static
       address 10.21.0.18
       netmask 255.255.255.248
       gateway 10.21.0.17
```

#### Jipangu
```
auto eth0
iface eth0 inet static
       address 10.21.0.19
       netmask 255.255.255.248
       gateway 10.21.0.17
```

