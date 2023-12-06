# Jarkom-Modul-4-A15-2023

### Kelompok A15

| **No** | **Nama**                   | **NRP**    |
| ------ | -------------------------- | ---------- |
| 1      | Frederick Hidayat          | 5025211152 |
| 2      | Reyner Fernaldi            | 5025201094 |


# PEMBAHASAN

## GNS VLSM
### Topologi GNS VLSM
</br><img src="img/gns.png?raw=true" alt="Alt text" title="1a" width="700">

### Rute
Rute yang kami gunakan adalah
</br><img src="img/rute1.png?raw=true" alt="Alt text" title="1a" width="500">

### Tree
</br><img src="img/tree_vlsm.jpeg?raw=true" alt="Alt text" title="1a" width="700">

### Pembagian IP
</br><img src="img/ip_vlsm.png?raw=true" alt="Alt text" title="1a" width="500">

### Konfigurasi
-   Aura
    ```
    auto eth0
    iface eth0 inet dhcp

    auto eth1
    iface eth1 inet static
        address 192.176.24.117
        netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
        address 192.176.24.125
        netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
        address 192.176.24.113
        netmask 255.255.255.252

    # Eisen10
    # A3
    up route add -net 192.176.24.120 netmask 255.255.255.252 gw 192.176.24.126
    # A5
    up route add -net 192.176.24.128 netmask 255.255.255.252 gw 192.176.24.126
    # A6
    up route add -net 192.176.24.132 netmask 255.255.255.252 gw 192.176.24.126
    # A7
    up route add -net 192.176.24.136 netmask 255.255.255.252 gw 192.176.24.126
    # A15
    up route add -net 192.176.12.0 netmask 255.255.252.0 gw 192.176.24.126
    # A16
    up route add -net 192.176.24.0 netmask 255.255.255.192 gw 192.176.24.126
    # A17
    up route add -net 192.176.24.104 netmask 255.255.255.248 gw 192.176.24.126
    # A18
    up route add -net 192.176.20.0 netmask 255.255.254.0 gw 192.176.24.126
    # A19
    up route add -net 192.176.22.0 netmask 255.255.255.0 gw 192.176.24.126
    # A20
    up route add -net 192.176.16.0 netmask 255.255.252.0 gw 192.176.24.126

    # Denken1
    # A21
    up route add -net 192.176.23.0 netmask 255.255.255.0 gw 192.176.24.118

    # Frieren7
    # A08-09-10
    up route add -net 192.176.24.140 netmask 255.255.255.252 gw 192.176.24.114
    up route add -net 192.176.24.144 netmask 255.255.255.252 gw 192.176.24.114
    up route add -net 192.176.24.148 netmask 255.255.255.252 gw 192.176.24.114

    # A11-12-13-14
    up route add -net 192.176.24.64 netmask 255.255.255.224 gw 192.176.24.114
    up route add -net 192.176.0.0 netmask 255.255.248.0 gw 192.176.24.114
    up route add -net 192.176.8.0 netmask 255.255.252.0 gw 192.176.24.114
    up route add -net 192.176.24.96 netmask 255.255.255.248 gw 192.176.24.114
    ```
-   Frieren
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.114
        netmask 255.255.255.252
        gateway 192.176.24.113

    auto eth1
    iface eth1 inet static
        address 192.176.24.65
        netmask 255.255.255.224

    auto eth2
    iface eth2 inet static
        address 192.176.24.145
        netmask 255.255.255.252


    up route add -net 192.176.24.140 netmask 255.255.255.252 gw 192.176.24.146
    up route add -net 192.176.24.148 netmask 255.255.255.252 gw 192.176.24.146

    up route add -net 192.176.0.0 netmask 255.255.248.0 gw 192.176.24.146
    up route add -net 192.176.8.0 netmask 255.255.252.0 gw 192.176.24.146
    up route add -net 192.176.24.96 netmask 255.255.255.248 gw 192.176.24.146

    ```
-   Flamme
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.146
        netmask 255.255.255.252
        gateway 192.176.24.145

    auto eth1
    iface eth1 inet static
        address 192.176.24.149
        netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
        address 192.176.24.141
        netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
        address 192.176.8.1
        netmask 255.255.252.0

    up route add -net 192.176.0.0 netmask 255.255.248.0 gw 192.176.24.150
    up route add -net 192.176.24.96 netmask 255.255.255.248 gw 192.176.24.142
    ```
-   Fern
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.150
        netmask 255.255.255.252
        gateway 192.176.24.149

    auto eth1
    iface eth1 inet static
        address 192.176.0.1
        netmask 255.255.248.0
    ```

-   Himmel
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.142
        netmask 255.255.255.252
        gateway 192.176.24.141

    auto eth1
    iface eth1 inet static
        address 192.176.24.97
        netmask 255.255.255.248
    ```
-   Eisen
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.126
        netmask 255.255.255.252
            gateway 192.176.24.125

    auto eth1
    iface eth1 inet static
        address 192.176.24.105
        netmask 255.255.255.248

    auto eth2
    iface eth2 inet static
        address 192.176.24.129
        netmask 255.255.255.252

    auto eth3
    iface eth3 inet static
        address 192.176.24.121
        netmask 255.255.255.252

    auto eth4
    iface eth4 inet static
        address 192.176.24.137
        netmask 255.255.255.252

    # A6
    up route add -net 192.176.24.132 netmask 255.255.255.252 gw 192.176.24.130
    # A15
    up route add -net 192.176.12.0 netmask 255.255.252.0 gw 192.176.24.130
    # A16
    up route add -net 192.176.24.0 netmask 255.255.255.192 gw 192.176.24.130
    # A18
    up route add -net 192.176.20.0 netmask 255.255.254.0 gw 192.176.24.130

    # A19
    up route add -net 192.176.22.0 netmask 255.255.255.0 gw 192.176.24.138
    # A20
    up route add -net 192.176.16.0 netmask 255.255.252.0 gw 192.176.24.138
    ```
-   Lugner
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.138
        netmask 255.255.255.252
            gateway 192.176.24.137

    auto eth1
    iface eth1 inet static
        address 192.176.22.1
        netmask 255.255.255.0

    auto eth2
    iface eth2 inet static
        address 192.176.16.1
        netmask 255.255.252.0
    ```

-   Linnie
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.130
        netmask 255.255.255.252
        gateway 192.176.24.129

    auto eth1
    iface eth1 inet static
        address 192.176.24.133
        netmask 255.255.255.252

    auto eth2
    iface eth2 inet static
        address 192.176.20.1
        netmask 255.255.254.0

    up route add -net 192.176.24.0 netmask 255.255.255.192 gw 192.176.24.134
    up route add -net 192.176.12.0 netmask 255.255.252.0 gw 192.176.24.134
    ```

-   Lawine
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.134
        netmask 255.255.255.252
        gateway 192.176.24.133

    auto eth1
    iface eth1 inet static
        address 192.176.24.1
        netmask 255.255.255.192
    ```

    up route add -net 192.176.12.0 netmask 255.255.252.0 gw 192.176.24.3

-   Heiter
    ```
    auto eth0
    iface eth0 inet static
        address 192.176.24.3
        netmask 255.255.255.192
        gateway 192.176.24.1

    auto eth1
    iface eth1 inet static
        address 192.176.12.1
        netmask 255.255.252.0
    ```

### Testing
Melakuakn ping dari GranzChannel ke AppetitRegion
</br><img src="img/test_gns.png?raw=true" alt="Alt text" title="1a" width="500">


## Topologi CPT CIDR
</br><img src="img/cpt.png?raw=true" alt="Alt text" title="1a" width="700">

## Penggabungan 1
</br><img src="img/P1T.png?raw=true" alt="Alt text" title="1a" width="500">
</br><img src="img/P1G.jpeg?raw=true" alt="Alt text" title="1a" width="700">

## Penggabungan 2
</br><img src="img/P2T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P2G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 3
</br><img src="img/P3T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P3G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 4
</br><img src="img/P4T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P4G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 5
</br><img src="img/P5T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P5G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 6
</br><img src="img/P6T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P6G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 7
</br><img src="img/P7T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P7G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 8
</br><img src="img/P8T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P8G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Penggabungan 9
</br><img src="img/P9T.png?raw=true" alt="Alt text" title="pp" width="500">
</br><img src="img/P9G.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Tree
</br><img src="img/tree_cidr.jpeg?raw=true" alt="Alt text" title="pp" width="700">

## Pembagian IP
</br><img src="img/ip_cidr.png?raw=true" alt="Alt text" title="pp" width="700">