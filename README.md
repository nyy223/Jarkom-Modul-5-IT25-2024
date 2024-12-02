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
### LuminaSquare, BalletTwins, SixStreet, OuterRing sebagai DNS Relay
>dhcprelay.sh
```
echo 'SERVERS="10.76.2.11"
INTERFACES="eth0 eth1 eth2 eth3"
OPTIONS=""
' > /etc/default/isc-dhcp-relay

echo 'net.ipv4.ip_forward=1' >> /etc/sysctl.conf

service isc-dhcp-relay restart
```
### Fairy sebagai DHCP Server
>dhcpserver.sh
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
### HDD sebagai DNS Server
>dnsserver.sh
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
### HIA, HollowZero sebagai Webserver
>webserver.sh
```
apt-get update
apt-get install apache2 netcat -y

service apache2 start

echo 'Welcome to {hostname}' > /var/www/html/index.html

service apache2 restart
```

## Misi 2 No. 2
Ketikkan command berikut di web console milik Fairy
```
iptables -A INPUT -p icmp --icmp-type echo-request -j DROP
```

```
iptables -A OUTPUT -p icmp --icmp-type echo-request -j ACCEPT
```

#### Test ping dari fairy ke node lain
<img width="595" alt="Screenshot 2024-12-01 at 19 33 20" src="https://github.com/user-attachments/assets/1c2ccf33-795c-4014-a720-71bb7de84f0d">

#### Test ping node lain ke fairy
<img width="504" alt="Screenshot 2024-12-01 at 19 33 29" src="https://github.com/user-attachments/assets/7f9e3730-190a-49a7-bdeb-d5cd794b2dd1">

## Misi 2 No. 3
### Buat konfigurasi iptables untuk melarang ping dari semua jaringan, lalu tambahkan ip Fairy agar diijinkan ping
```
iptables -P INPUT DROP
```

```
iptables -A INPUT -s 10.76.2.11 -j ACCEPT
```

### Tes dengan ping
#### Fairy bisa ping HDD
<img width="999" alt="Screenshot 2024-12-01 at 22 18 38" src="https://github.com/user-attachments/assets/590ff0a6-f178-401a-8a06-c7c2d7ba403a">

#### Selain Fairy tidak bisa ping HDD
<img width="1002" alt="Screenshot 2024-12-01 at 22 19 39" src="https://github.com/user-attachments/assets/6dac38e6-f438-46da-ad56-33597cf3017a">

### Tes dengan netcat
### Lakukan tes nc di SixStreet
<img width="999" alt="Screenshot 2024-12-01 at 22 20 18" src="https://github.com/user-attachments/assets/795c1757-c169-4189-9036-b7b1bc54ebbe">

### Lakukan tes nc di Fairy
<img width="995" alt="Screenshot 2024-12-01 at 22 20 40" src="https://github.com/user-attachments/assets/830ed844-0e51-44bc-8a19-7b630265aa44">

### nc yang diterima oleh HDD hanya dari Fairy
<img width="468" alt="Screenshot 2024-12-01 at 22 22 03" src="https://github.com/user-attachments/assets/24d2fa6a-29df-4168-b033-b34fb227eb31">

## Misi 2 No. 4
Ketikkan command berikut di web console HollowZero
```
iptables -P INPUT DROP
```
```
iptables -A INPUT -s 10.76.2.64/26 -m time --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
```
iptables -A INPUT -s 10.76.1.0/26 -m time --weekdays Mon,Tue,Wed,Thu,Fri -j ACCEPT
```
#### Test Burnice ping ke HollowZero tapi gabisa karena sekarang Minggu
<img width="518" alt="Screenshot 2024-12-01 at 20 15 55" src="https://github.com/user-attachments/assets/a4fc47c4-3399-4ba6-87a7-5e9c8876b605">

Coba ubah aturannya agar mengizinkan hari minggu dengan mengetikkan command
```
iptables -A INPUT -s 10.76.2.64/26 -m time --weekdays Sun -j ACCEPT
```

#### Test Burnice ping dan curl ke HollowZero dan sudah bisa :D
<img width="614" alt="Screenshot 2024-12-01 at 20 39 21" src="https://github.com/user-attachments/assets/920b6dc8-6458-4f4a-bd98-2f0a6504709a">

## Misi 2 No. 5
Ketikkan command berikut di web console HIA
```
iptables -P INPUT DROP
```
```
iptables -A INPUT -s 10.76.0.128/25 -m time --timestart 08:00 --timestop 21:00 -j ACCEPT
```
```
iptables -A INPUT -s 10.76.1.0/24 -m time --timestart 03:00 --timestop 23:00 -j ACCEPT
```

#### Test Lycaon dan Jane curl ke HIA masih bisa karena masih dalam waktu yang diperbolehkan
<img width="316" alt="Screenshot 2024-12-01 at 20 47 03" src="https://github.com/user-attachments/assets/02d054bb-620a-42fc-9b9d-eaf01e52fe27">
<img width="315" alt="Screenshot 2024-12-01 at 20 47 31" src="https://github.com/user-attachments/assets/7de5f032-509d-442d-8605-a33e19ad8d01">

## Misi 2 No. 6
### Buat konfigurasi untuk memblokir aktivitas port scanning yang melebihi 25 port dalam rentang 10 detik, penyerang yang diblokir tidak bisa ping, nc, atau curl ke HIA, log dari iptables akan tercatat untuk analisis.
```
# Atur rate limit untuk port scanning (maksimum 25 koneksi per 10 detik)
iptables -N PORTSCAN
iptables -A INPUT -p tcp --dport 1:100 -m state --state NEW -m recent --set --name portscan
iptables -A INPUT -p tcp --dport 1:100 -m state --state NEW -m recent --update --seconds 10 --hitcount 25 --name portscan -j PORTSCAN

# Blokir IP yang terdeteksi melakukan port scanning tidak wajar
iptables -A PORTSCAN -m recent --set --name blacklist
iptables -A PORTSCAN -j DROP

# Blokir semua aktivitas dari IP yang ada di daftar blacklist
iptables -A INPUT -m recent --name blacklist --rcheck -j REJECT
iptables -A OUTPUT -m recent --name blacklist --rcheck -j REJECT

# Logging untuk port scanning
iptables -A PORTSCAN -j LOG --log-prefix='PORT SCAN DETECTED' --log-level 4
```
### Tes melakukan nmap dengan Jane, maka otomatis akan terblokir dan tidak bisa curl
<img width="618" alt="Screenshot 2024-12-02 at 02 42 10" src="https://github.com/user-attachments/assets/ab3e4856-4c5d-49ab-aebd-49ded6cd193d">

### Tetap bisa curl dengan Policeboo
<img width="573" alt="Screenshot 2024-12-02 at 02 42 20" src="https://github.com/user-attachments/assets/ea424173-91f6-4c3f-a39e-b8a75950ad37">

### Tes netcat
#### Jane akan terblokir dan tidak bisa nc
<img width="844" alt="Screenshot 2024-12-02 at 02 43 22" src="https://github.com/user-attachments/assets/773deacc-425e-41ca-9d6a-2f53a6910d61">

#### Policeboo tetap bisa nc seperti biasa
<img width="842" alt="Screenshot 2024-12-02 at 02 43 46" src="https://github.com/user-attachments/assets/26fbea32-291f-4e41-b927-bc6246ab74a3">


## Misi 2 No. 7
Masuk ke web console HollowZero dan ketikkan command
```
iptables -A INPUT -p tcp --dport http -m conntrack --ctstate NEW -m recent --set
```
```
iptables -A INPUT -p tcp --dport http -m conntrack --ctstate NEW -m recent --update --seconds 1 --hitcount 3 -j REJECT
```
```
iptables -A INPUT -p tcp --dport http -j ACCEPT
```

#### Coba test dari web console client mana saja, ketikkan command
```
parallel curl -s 10.76.2.130 ::: 10.76.2.68 10.76.2.67 10.76.1.3 10.76.1.2
```
<img width="830" alt="Screenshot 2024-12-02 at 02 44 25" src="https://github.com/user-attachments/assets/1afef3b0-76f3-46bf-8255-8a9c89ad3a74">

Terlihat bahwa hanya 2 koneksi yang bisa curl

## Misi 2 No. 8
### Buat konfigurasi agar setiap paket yang dikirim Fairy ke Burnice akan dialihkan ke HollowZero
```
iptables -t nat -A PREROUTING -p tcp -j DNAT --to-destination 10.76.2.130 --dport 3030
iptables -A FORWARD -p tcp -d 10.76.2.130 -j ACCEPT
```

### Tes mengirim paket dari Fairy ke Burnice
<img width="530" alt="Screenshot 2024-12-02 at 02 45 16" src="https://github.com/user-attachments/assets/271a2721-4420-4b5a-880c-647c6ef8958b">

### Cek dengan tcpdump di HollowZero untuk mengetahui apakah ada paket masuk
`tcpdump -i eth0 host 10.76.2.11 and port 3030`
<img width="758" alt="Screenshot 2024-12-02 at 02 45 25" src="https://github.com/user-attachments/assets/314933c6-0aab-4cd6-9da3-6891c08b0875">

## Misi 3
### Buat konfigurasi burnice tidak bisa mengirim atau menerima paket
```
iptables --policy INPUT DROP
iptables --policy OUTPUT DROP
iptables --policy FORWARD DROP
```
### Tes
#### Burnice ping ke client lain
<img width="757" alt="Screenshot 2024-12-02 at 02 46 20" src="https://github.com/user-attachments/assets/46615d8c-d6da-44db-af5c-a12b4b8b8097">

### Client lain ping ke burnice
<img width="756" alt="Screenshot 2024-12-02 at 02 46 44" src="https://github.com/user-attachments/assets/b7d878be-19b7-4493-a3c5-26ad0537ab82">
