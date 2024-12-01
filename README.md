# Jarkom-Modul-5-IT25-2024

# Anggota Kelompok
| Nama  | NRP  |
|----------|----------|
| Fikri Aulia As Sa'adi  | 5027231026 |
| Nayla Raissa Azzahra  | 5027231054 |

## Topologi
<img width="1113" alt="Screenshot 2024-12-01 at 15 28 32" src="https://github.com/user-attachments/assets/8f05bdf0-b3ce-46ea-8bf6-4596b6aad104">

## Pembagian Subnet
<img width="922" alt="Screenshot 2024-12-01 at 12 27 40" src="https://github.com/user-attachments/assets/d2ef08e0-6ea0-4ece-b3c8-641695fe69f3">

## Misi 1 No. 1-3
### NewEridu
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
  address 10.76.0.1
  netmask 255.255.255.252
  
auto eth2
iface eth2 inet static
  address 10.76.0.5
  netmask 255.255.255.252

#A6
post-up route add -net 10.76.2.0 netmask 255.255.255.248 gw 10.76.0.2

#A3
post-up route add -net 10.76.0.8 netmask 255.255.255.248 gw 10.76.06

#A8
post-up route add -net 10.76.2.64 netmask 255.255.255.192 gw 10.76.0.2

#A7
post-up route add -net 10.76.2.8 netmask 255.255.255.248 gw 10.76.0.2

#A4
post-up route add -net 10.76.0.128 netmask 255.255.255.128 gw 10.76.0.6

#A5
post-up route add -net 10.76.1.0 netmask 255.255.255.0 gw 10.76.0.6

#A9
post-up route add -net 10.76.2.128 netmask 255.255.255.252 gw 10.76.0.2
```
### LuminaSquare
```
auto eth0
iface eth0 inet static
  address 10.76.0.6
  netmask 255.255.255.252
  gateway 10.76.0.5

auto eth1
iface eth1 inet static
  address 10.76.0.9
  netmask 255.255.255.248
 
auto eth2
iface eth2 inet static
  address 10.76.1.1
  netmask 255.255.255.0

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A1
post-up route add -net 10.76.0.0 netmask 255.255.255.252 gw 10.76.0.5

#A4
post-up route add -net 10.76.0.128 netmask 255.255.255.128 gw 10.76.0.11

#A7
post-up route add -net 10.76.2.8 netmask 255.255.255.248 gw 10.76.0.5
```
### BalletTwins
```
auto eth0
iface eth0 inet static
  address 10.76.0.11
  netmask 255.255.255.248
  gateway 10.76.0.9
 
auto eth1
iface eth1 inet static
  address 10.76.0.129
  netmask 255.255.255.128

up echo nameserver 192.168.122.1 > /etc/resolv.conf
 
#A2
post-up route add -net 10.76.0.4 netmask 255.255.255.252 gw 10.76.0.9

#A1
post-up route add -net 10.76.0.0 netmask 255.255.255.252 gw 10.76.0.9

#A7
post-up  route add -net 10.76.2.8 netmask 255.255.255.248 gw 10.76.0.9
```
### SixStreet
```
auto eth0
iface eth0 inet static
  address 10.76.0.2
  netmask 255.255.255.252
  gateway 10.76.0.1

auto eth1
iface eth1 inet static
  address 10.76.2.1
  netmask 255.255.255.248

auto eth2
iface eth2 inet static
  address 10.76.2.9
  netmask 255.255.255.248

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A8
post-up route add -net 10.76.2.64 netmask 255.255.255.192 gw 10.76.2.3

#A9
post-up route add -net 10.76.2.128 netmask 255.255.255.252 gw 10.76.2.2

#A4
post-up route add -net 10.76.0.128 netmask 255.255.255.128 gw 10.76.0.1
```
### OuterRing
```
auto eth0
iface eth0 inet static
  address 10.76.2.3
  netmask 255.255.255.248
  gateway 10.76.2.1

auto eth1
iface eth1 inet static
  address 10.76.2.65
  netmask 255.255.255.192

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A9
post-up route add -net 10.76.2.128 netmask 255.255.255.252 gw 10.76.2.2

#A1
post-up route add -net 10.76.0.0 netmask 255.255.255.252 gw 10.76.2.1

#A7
post-up route add -net 10.76.2.8 netmask 255.255.255.248 gw 10.76.2.1
```
### ScootOutpost
```
auto eth0
iface eth0 inet static
  address 10.76.2.2
  netmask 255.255.255.248
  gateway 10.76.2.1

auto eth1
iface eth1 inet static
  address 10.76.2.129
  netmask 255.255.255.252

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A2
post-up route add -net 10.76.0.4 netmask 255.255.255.252 gw 10.76.2.1

#A8
post-up route add -net 10.76.2.16 netmask 255.255.255.192 gw 10.76.2.3

#A1
post-up  route add -net 10.76.0.0 netmask 255.255.255.252 gw 10.76.2.1
```
### Fairy
```
auto eth0
iface eth0 inet static
  address 10.76.2.11
  netmask 255.255.255.248
  gateway 10.76.2.9

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A8
post-up route add -net 10.76.2.16 netmask 255.255.255.192 gw 10.76.2.9

#A4
post-up route add -net 10.76.0.128 netmask 255.255.255.128 gw 10.76.2.9
```
### Jane, Policeboo, Ellen, Lyacon, Caesar, Burnice
```
auto eth0
iface eth0 inet dhcp
```
### HIA
```
auto eth0
iface eth0 inet static
  address 10.76.0.10
  netmask 255.255.255.248
  gateway 10.76.0.9
 
up echo nameserver 192.168.122.1 > /etc/resolv.conf
```
### HollowZero
```
auto eth0
iface eth0 inet static
  address 10.76.2.130
  netmask 255.255.255.252
  gateway 10.76.2.129

up echo nameserver 192.168.122.1 > /etc/resolv.conf

#A1
post-up route add -net 10.76.0.0 netmask 255.255.255.252 gw 10.76.2.129
```
### HDD
```
auto eth0
iface eth0 inet static
  address 10.76.2.10
  netmask 255.255.255.248
  gateway 10.76.2.9

up echo nameserver 192.168.122.1 > /etc/resolv.conf
```



