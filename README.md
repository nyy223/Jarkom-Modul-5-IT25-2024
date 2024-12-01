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

## Misi 2 No. 1
Tambahkan command berikut di bashrc
```
ETH0_IP=$(ip -4 addr show eth0 | grep -oP '(?<=inet\s)\d+(\.\d+){3}')
iptables -t nat -A POSTROUTING -o eth0 -j SNAT --to-source $ETH0_IP
```

## Misi 1 No. 4
### LuminaSquare, BalletTwins, SixStreet, OuterRing
```
echo 'SERVERS="10.76.2.11"
INTERFACES="eth0 eth1 eth2 eth3"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

echo 'net.ipv4.ip_forward=1' >> /etc/sysctl.conf

service isc-dhcp-relay restart
```
### Fairy
```
apt-get update
apt-get install isc-dhcp-server netcat -y

echo 'INTERFACESv4="eth0"' > /etc/default/isc-dhcp-server

echo '#A8
subnet 10.76.2.64 netmask 255.255.255.192 {
  range 10.76.2.66 10.76.2.125;
  option routers 10.76.2.65;
  option broadcast-address 10.76.2.126;
  option domain-name-servers 10.76.2.10;
  default-lease-time 600;
  max-lease-time 7200;
}

#A4
subnet 10.76.0.128 netmask 255.255.255.128 {
  range 10.76.0.130 10.76.0.253;
  option routers 10.76.0.129;
  option broadcast-address 10.76.0.254;
  option domain-name-servers 10.76.2.10;
  default-lease-time 600;
  max-lease-time 7200;
}

#A5
subnet 10.76.1.0 netmask 255.255.255.0 {
  range 10.76.1.2 10.76.1.253;
  option routers 10.76.1.1;
  option broadcast-address 10.76.1.254;
  option domain-name-servers 10.76.2.10;
  default-lease-time 600;
  max-lease-time 7200;
}


subnet 10.76.0.0 netmask 255.255.255.252 {}
subnet 10.76.0.4 netmask 255.255.255.252 {}
subnet 10.76.0.8 netmask 255.255.255.248 {}
subnet 10.76.2.0 netmask 255.255.255.248 {}
subnet 10.76.2.8 netmask 255.255.255.248 {}
subnet 10.76.2.128 netmask 255.255.255.252 {}
' > /etc/dhcp/dhcpd.conf

service isc-dhcp-server restart
```
### HDD
```
apt-get update
apt-get install bind9 netcat -y

echo 'options {
        directory "/var/cache/bind";

        forwarders {
                192.168.122.1;
        };

        // dnssec-validation auto;
        allow-query{any;};
        auth-nxdomain no;
        listen-on-v6 { any; };
}; ' >/etc/bind/named.conf.options

service bind9 restart
```
### HIA, HollowZero
```
apt-get update
apt-get install apache2 netcat -y

service apache2 start

echo 'Welcome to {hostname}' > /var/www/html/index.html

service apache2 restart
```

## Misi 2 No. 2
Ketikkan command berikut di web console milik Fairy
`iptables -A INPUT -p icmp --icmp-type echo-request -j DROP`

`iptables -A OUTPUT -p icmp --icmp-type echo-request -j ACCEPT`
#### Test ping dari fairy ke node lain
<img width="595" alt="Screenshot 2024-12-01 at 19 33 20" src="https://github.com/user-attachments/assets/1c2ccf33-795c-4014-a720-71bb7de84f0d">

#### Test ping node lain ke fairy
<img width="504" alt="Screenshot 2024-12-01 at 19 33 29" src="https://github.com/user-attachments/assets/7f9e3730-190a-49a7-bdeb-d5cd794b2dd1">
