
# Jarkom-Modul-5-IT13-2023

|       Nama      | NRP        | 
| -----------     | :---------: 
| Della Setyowati | 5027211044 | 
| Wisnu Adjie Saka| 5027211051 | 

## Daftar Isi
- [Topologi](#topologi)
- [VLSM](#vlsm)

## <a name="topologi"></a> Topologi
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1186964708239089664/WhatsApp_Image_2023-12-20_at_15.29.34_520172ac.jpg?ex=65952a07&is=6582b507&hm=80165c95a4ffc2b919ff61d79cb5dbabbdd21a48037a66a390385be71b350a5e&)

### VLSM
Untuk membuat VLSM, pertama-tama, kita perlu membuat tabel yang berisi jumlah IP pada setiap subnet
![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1186966257237495818/image.png?ex=65952b78&is=6582b678&hm=7afdec5073a652cdc0170df6bbed5fdcfe7cecfa0c6543049150534b6b826d62&)


### Pembagian IP
Berdasarkan Perhitungan IP maka didapatkan pembagian IP sebagai berikut

![untitled](https://cdn.discordapp.com/attachments/901344920361656355/1186966863746433094/image.png?ex=65952c09&is=6582b709&hm=b9d3bbc604a6cf9a512fa2320961d3f71b06e7a5d0123b7daa3abc4178f702f2&)

### Konfigurasi Pada VLSM
- Aura
```
# config for eth0
#auto eth0
#iface eth0 inet dhcp
auto eth0
iface eth0 inet static
    address 192.168.122.2
    netmask 255.255.255.252
    gateway 192.168.122.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf

# config for eth1
auto eth1
iface eth1 inet static
    address 10.70.14.133
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 10.70.14.129
    netmask 255.255.255.252
```
- Fern
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.3
    netmask 255.255.255.128
    gateway 10.70.14.1

# config for eth1
auto eth1
iface eth1 inet static
    address 10.70.14.145
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 10.70.14.149
    netmask 255.255.255.252

```
- Frieren
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.134
    netmask 255.255.255.252
    gateway 10.70.14.133
    
# config for eth1
auto eth1
iface eth1 inet static
    address 10.70.14.137
    netmask 255.255.255.252

# config for eth2
auto eth2
iface eth2 inet static
    address 10.70.14.141
    netmask 255.255.255.252
```
- Heiter
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.130
    netmask 255.255.255.252
    gateway 10.70.14.129

# config for eth1
auto eth1
iface eth1 inet static
    address 10.70.0.1
    netmask 255.255.248.0

# config for eth2
auto eth2
iface eth2 inet static
    address 10.70.8.1
    netmask 255.255.252.0
```
- Himmel
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.142
    netmask 255.255.255.252
    gateway 10.70.14.141

# config for eth1
auto eth1
iface eth1 inet static
    address 10.70.12.1
    netmask 255.255.254.0

# config for eth2
auto eth2
iface eth2 inet static
    address 10.70.14.1
    netmask 255.255.255.128
```
- GrobeForest
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.8.3
    netmask 255.255.252.0
    gateway 10.70.8.1

auto eth0
iface eth0 inet dhcp
    gateway 10.70.8.1
```
- Sein
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.8.2
    netmask 255.255.252.0
    gateway 10.70.8.1
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```

- Richter (DNS Server)
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.146
    netmask 255.255.255.252
    gateway 10.70.14.145
```
- Revolter (DHCP Server)
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.150
    netmask 255.255.255.252
    gateway 10.70.14.149
```
- LaubHills 
```

# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.12.2
    netmask 255.255.254.0
    gateway 10.70.12.1

auto eth0
iface eth0 inet dhcp
    gateway 10.70.12.1
```
- SchwerMountains
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.2
    netmask 255.255.255.128
    gateway 10.70.14.1

auto eth0
iface eth0 inet dhcp
    gateway 10.70.14.1
```

- Stark 
```
  # config for eth0
auto eth0
iface eth0 inet static
    address 10.70.14.138
    netmask 255.255.255.252
    gateway 10.70.14.137
    up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
- Turk--Region
```
# config for eth0
auto eth0
iface eth0 inet static
    address 10.70.0.2
    netmask 255.255.248.0
    gateway 10.70.0.1

auto eth0
iface eth0 inet dhcp
    gateway 10.70.0.1
```
