# Jarkom-Modul-4-D09-2023

## Anggota Kelompok
| Nama | NRP |
|---------------------------|------------|
|Laurivasya Gadhing Syahafidh | 5025211136 | 
|Dafarel Fatih Wirayudha| 5025211120 |

## Daftar Isi
- [Pre-Requisites](#daftar-isi)
  - [Topologi PKT-VLSM](#topologi-pkt-cidr)
  - [Topologi GNS-CIDR](#topologi-gns-vlsm)
  - [Rute](#rute)

- [VLSM](#vlsm)
  - [Tree](#tree)
  - [Pembagian IP](#pembagian-ip)
  - [Hasil Testing VLSM](#testing)

- [CIDR](#cidr)
  - [Penggabungan IP](#penggabungan-ip)
  - [Tree](#tree-1)
  - [Pembagian IP](#pembagian-ip-1)
  - [Konfigurasi Network](#konfigurasi-network)
  - [Routing](#routing)
  - [Hasil Testing CIDR](#testing1)

  Kami mengimplementasikan `CIDR` dengan menggunakan `GNS3` dan `VLSM` dengan menggunakan `Cisco`

  ## Pre-requites
  ### Topologi PKT-VLSM
  ![topologi-cisco](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/image.png)
  ### Topologi GNS3-CIDR
  ![topologi-gns3](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/topologi-gns3.png)
  ### Rute
  > Prefix IP kelompok kami adalah **10.26**
 
  Hasil dari rute yang kami dapatkan adalah sebagai berikut :
  ![rute](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/rute.png)

  ## VLSM
  ### Tree
  Berikut hasil pemecahan ip dari subnet besar menjadi lebih kecil

  ![tree-vlsm](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/tree-vlsm.png)
  ### Pembagian IP
  Berikut hasil pembagian IP berdasarkan tree diatas

  ![ip-vlsm](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/ip%20vlsm.png)

  ### Pembagian IP per Node
  Berikut hasil pembagian IP per Node berdasarkan nid per subnet

  ![ip-vlsm-perNode](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/ip_node_vlsm.png)

  ### Routing VLSM
  * **Aura**
    ```
    10.26.23.0/24 via 10.26.24.150
    10.26.0.0/21 via 10.26.24.114
    10.26.8.0/22 via 10.26.24.114
    10.26.24.96/29 via 10.26.24.114
    10.26.24.104/29 via 10.26.24.130
    10.26.24.144/30 via 10.26.24.130
    10.26.16.0/22 via 10.26.24.130
    10.26.22.0/24 via 10.26.24.130
    10.26.24.0/26 via 10.26.24.130
    10.26.12.0/22 via 10.26.24.130
    10.26.20.0/23 via 10.26.24.130
    10.26.24.64/27 via 10.26.24.114
    10.26.24.116/30 via 10.26.24.114
    10.26.24.124/30 via 10.26.24.114
    10.26.24.120/30 via 10.26.24.114
    10.26.24.132/30 via 10.26.24.130
    10.26.24.136/30 via 10.26.24.130
    10.26.24.140/30 via 10.26.24.130
    ```
  * **Frieren**
    ```
    10.26.0.0/21 via 10.26.24.118
    10.26.8.0/22 via 10.26.24.118
    10.26.24.96/29 via 10.26.24.118
    10.26.23.0/24 via 10.26.24.113
    10.26.24.144/30 via 10.26.24.113
    10.26.24.104/29 via 10.26.24.113
    10.26.16.0/22 via 10.26.24.113
    10.26.22.0/24 via 10.26.24.113
    10.26.24.0/26 via 10.26.24.113
    10.26.12.0/22 via 10.26.24.113
    10.26.20.0/23 via 10.26.24.113
    0.0.0.0/0 via 10.26.24.113
    10.26.24.120/30 via 10.26.24.118
    10.26.24.124/30 via 10.26.24.118
    10.26.24.148/30 via 10.26.24.113
    10.26.24.128/30 via 10.26.24.113
    10.26.24.132/30 via 10.26.24.113
    10.26.24.140/30 via 10.26.24.113
    10.26.24.136/30 via 10.26.24.113
    ```
  * **Flamme**
    ```
    10.26.24.96/29 via 10.26.24.126
    10.26.0.0/21 via 10.26.24.122
    10.26.24.64/27 via 10.26.24.117
    10.26.23.0/24 via 10.26.24.117
    10.26.24.104/29 via 10.26.24.117
    10.26.24.144/30 via 10.26.24.117
    10.26.16.0/22 via 10.26.24.117
    10.26.22.0/24 via 10.26.24.117
    10.26.24.0/26 via 10.26.24.117
    10.26.12.0/22 via 10.26.24.117
    10.26.20.0/23 via 10.26.24.117
    10.26.24.112/30 via 10.26.24.117
    10.26.24.148/30 via 10.26.24.117
    10.26.24.128/30 via 10.26.24.117
    10.26.24.132/30 via 10.26.24.117
    10.26.24.140/30 via 10.26.24.117
    10.26.24.136/30 via 10.26.24.117
    ```
  * **Fern**
    ```
    10.26.8.0/22 via 10.26.24.121
    10.26.24.96/29 via 10.26.24.121
    10.26.24.64/27 via 10.26.24.121
    10.26.23.0/24 via 10.26.24.121
    10.26.24.104/29 via 10.26.24.121
    10.26.24.144/30 via 10.26.24.121
    10.26.16.0/22 via 10.26.24.121
    10.26.22.0/24 via 10.26.24.121
    10.26.24.0/26 via 10.26.24.121
    10.26.12.0/22 via 10.26.24.121
    10.26.20.0/23 via 10.26.24.121
    10.26.24.124/30 via 10.26.24.121
    10.26.24.112/30 via 10.26.24.121
    10.26.24.148/30 via 10.26.24.121
    10.26.24.116/30 via 10.26.24.121
    10.26.24.128/30 via 10.26.24.121
    10.26.24.132/30 via 10.26.24.121
    10.26.24.140/30 via 10.26.24.121
    10.26.24.136/30 via 10.26.24.121
    ```
  * **Himmel**
    ```
    10.26.8.0/22 via 10.26.24.125
    10.26.0.0/21 via 10.26.24.125
    10.26.24.64/27 via 10.26.24.125
    10.26.23.0/24 via 10.26.24.125
    10.26.24.104/29 via 10.26.24.125
    10.26.24.144/30 via 10.26.24.125
    10.26.16.0/22 via 10.26.24.125
    10.26.22.0/24 via 10.26.24.125
    10.26.24.0/26 via 10.26.24.125
    10.26.12.0/22 via 10.26.24.125
    10.26.20.0/23 via 10.26.24.125
    10.26.24.120/30 via 10.26.24.125
    10.26.24.116/30 via 10.26.24.125
    10.26.24.112/30 via 10.26.24.125
    10.26.24.148/30 via 10.26.24.125
    10.26.24.128/30 via 10.26.24.125
    10.26.24.132/30 via 10.26.24.125
    10.26.24.140/30 via 10.26.24.125
    10.26.24.136/30 via 10.26.24.125
    ```
  * **Denken**
    ```
    10.26.0.0/21 via 10.26.24.149
    10.26.8.0/22 via 10.26.24.149
    10.26.24.96/29 via 10.26.24.149
    10.26.24.104/29 via 10.26.24.149
    10.26.24.144/30 via 10.26.24.149
    10.26.16.0/22 via 10.26.24.149
    10.26.22.0/24 via 10.26.24.149
    10.26.24.0/26 via 10.26.24.149
    10.26.12.0/22 via 10.26.24.149
    10.26.20.0/23 via 10.26.24.149
    10.26.24.64/27 via 10.26.24.149
    0.0.0.0/0 via 10.26.24.149
    10.26.24.112/30 via 10.26.24.149
    10.26.24.116/30 via 10.26.24.149
    10.26.24.124/30 via 10.26.24.149
    10.26.24.120/30 via 10.26.24.149
    10.26.24.128/30 via 10.26.24.149
    10.26.24.132/30 via 10.26.24.149
    10.26.24.136/30 via 10.26.24.149
    10.26.24.140/30 via 10.26.24.149
    ```
  * **Eisen**
    ```
    10.26.0.0/21 via 10.26.24.129
    10.26.8.0/22 via 10.26.24.129
    10.26.24.96/29 via 10.26.24.129
    10.26.23.0/24 via 10.26.24.129
    10.26.22.0/24 via 10.26.24.142
    10.26.16.0/22 via 10.26.24.142
    10.26.20.0/23 via 10.26.24.134
    10.26.24.0/26 via 10.26.24.134
    10.26.12.0/22 via 10.26.24.134
    10.26.24.64/27 via 10.26.24.129
    0.0.0.0/0 via 10.26.24.129
    10.26.24.112/30 via 10.26.24.129
    10.26.24.148/30 via 10.26.24.129
    10.26.24.116/30 via 10.26.24.129
    10.26.24.120/30 via 10.26.24.129
    10.26.24.124/30 via 10.26.24.129
    10.26.24.136/30 via 10.26.24.134
    ```
  * **Lugner**
    ```
    10.26.0.0/21 via 10.26.24.141
    10.26.8.0/22 via 10.26.24.141
    10.26.24.96/29 via 10.26.24.141
    10.26.24.104/29 via 10.26.24.141
    10.26.24.144/30 via 10.26.24.141
    10.26.23.0/24 via 10.26.24.141
    10.26.20.0/23 via 10.26.24.141
    10.26.24.0/26 via 10.26.24.141
    10.26.12.0/22 via 10.26.24.141
    10.26.24.64/27 via 10.26.24.141
    10.26.24.112/30 via 10.26.24.141
    10.26.24.120/30 via 10.26.24.141
    10.26.24.124/30 via 10.26.24.141
    10.26.24.128/30 via 10.26.24.141
    10.26.24.132/30 via 10.26.24.141
    10.26.24.136/30 via 10.26.24.141
    10.26.24.148/30 via 10.26.24.141
    10.26.24.116/30 via 10.26.24.141
    ```
  * **Linie**
    ```
    10.26.24.0/26 via 10.26.24.138
    10.26.12.0/22 via 10.26.24.138
    10.26.24.104/29 via 10.26.24.133
    10.26.16.0/22 via 10.26.24.133
    10.26.22.0/24 via 10.26.24.133
    10.26.24.144/30 via 10.26.24.133
    10.26.0.0/21 via 10.26.24.133
    10.26.8.0/22 via 10.26.24.133
    10.26.24.96/29 via 10.26.24.133
    10.26.23.0/24 via 10.26.24.133
    10.26.24.64/27 via 10.26.24.133
    10.26.24.140/30 via 10.26.24.133
    10.26.24.128/30 via 10.26.24.133
    10.26.24.148/30 via 10.26.24.133
    10.26.24.112/30 via 10.26.24.133
    10.26.24.116/30 via 10.26.24.133
    10.26.24.120/30 via 10.26.24.133
    10.26.24.124/30 via 10.26.24.133
    ```
  * **Lawine**
   ```
   10.26.12.0/22 via 10.26.24.3
   10.26.20.0/23 via 10.26.24.137
   10.26.24.104/29 via 10.26.24.137
   10.26.16.0/22 via 10.26.24.137
   10.26.22.0/24 via 10.26.24.137
   10.26.24.144/30 via 10.26.24.137
   10.26.23.0/24 via 10.26.24.137
   10.26.0.0/21 via 10.26.24.137
   10.26.8.0/22 via 10.26.24.137
   10.26.24.96/29 via 10.26.24.137
   10.26.24.64/27 via 10.26.24.137
   10.26.24.128/30 via 10.26.24.137
   10.26.24.132/30 via 10.26.24.137
   10.26.24.140/30 via 10.26.24.137
   10.26.24.148/30 via 10.26.24.137
   10.26.24.112/30 via 10.26.24.137
   10.26.24.116/30 via 10.26.24.137
   10.26.24.120/30 via 10.26.24.137
   10.26.24.124/30 via 10.26.24.137
   ```
  * **Heiter**
   ```
   10.26.20.0/23 via 10.26.24.1
   10.26.24.104/29 via 10.26.24.1
   10.26.16.0/22 via 10.26.24.1
   10.26.22.0/24 via 10.26.24.1
   10.26.24.144/30 via 10.26.24.1
   10.26.23.0/24 via 10.26.24.1
   10.26.0.0/21 via 10.26.24.1
   10.26.8.0/22 via 10.26.24.1
   10.26.24.96/29 via 10.26.24.1
   10.26.24.64/27 via 10.26.24.1
   10.26.24.136/30 via 10.26.24.1
   10.26.24.132/30 via 10.26.24.1
   10.26.24.140/30 via 10.26.24.1
   10.26.24.148/30 via 10.26.24.1
   10.26.24.128/30 via 10.26.24.1
   10.26.24.112/30 via 10.26.24.1
   10.26.24.116/30 via 10.26.24.1
   10.26.24.120/30 via 10.26.24.1
   10.26.24.124/30 via 10.26.24.1
   ```
  ### Hasil Testing VLSM
  Berikut adalah hasil test simulasi kirim pdu dari node ke node
  ![pdu_hasil](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/kirim_pesan.png)
  Bisa dilihat di window simulation, pengiriman pdu dari lakekorridor ke willeregion, laubhills, frieren, dan granzchannel berjalan success

  Berikut adalah hasil ping dari RoyalCapital ke Stark (10.26.24.146)
  ![pdu_hasil](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/pingVLSM.png)
  
  ## CIDR
  ### Penggabungan IP
  ![topologi-gns3](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/topologi-gns3.png)
  
  ![1](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/Screenshot%202023-12-06%20at%2015.44.18.png)

  ![2](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/2.png)

  ![3](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/3.png)

  ![4](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/4.png)

  ![5](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/5.png)

  ![6](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/6.png)

  ![7](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/7.png)

  ![8](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/8.png)
  ### Tree
  Berikut hasil pemecahan ip dari subnet besar menjadi lebih kecil

  ![tree-cidr](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/tree-cidr.png)
  ### Pembagian IP
  Berikut hasil pembagian IP berdasarkan tree diatas

  ![ip-cidr](https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/blob/main/src-modul%204/ip%20cidr.png)
  ### Konfigurasi Network
* ### Router
    * **Aura**
    ``` 
            # Static config for eth0
            auto eth0
            iface eth0 inet dhcp

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.29.0.1
                netmask 255.255.255.252

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.28.128.1
                netmask 255.255.255.252

            # Static config for eth3
            auto eth3
            iface eth3 inet static
                address 10.27.0.1
                netmask 255.255.255.252
    ```

    * **Frieren**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.28.128.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.28.32.1
                netmask 255.255.255.252

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.28.64.1
                netmask 255.255.255.224
    ```

    * **Fern**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.28.0.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.28.8.1
                netmask 255.255.248.0
    ```

    * **Flamme**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.28.32.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.28.0.1
                netmask 255.255.255.252

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.28.24.1
                netmask 255.255.252.0

            # Static config for eth3
            auto eth3
            iface eth3 inet static
                address 10.28.16.1
                netmask 255.255.255.252
    ```

    * **Himmel**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.28.16.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.28.20.1
                netmask 255.255.255.248
    ```

    * **Denken**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.29.0.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.29.128.1
                netmask 255.255.255.0
    ```

    * **Eisen**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.27.0.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.26.192.1
                netmask 255.255.255.252

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.26.160.1
                netmask 255.255.255.252

            # Static config for eth3
            auto eth3
            iface eth3 inet static
                address 10.26.64.1
                netmask 255.255.255.248

            # Static config for eth4
            auto eth4
            iface eth4 inet static
                address 10.26.32.1
                netmask 255.255.255.252
    ```

    * **Lugner**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.26.160.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.26.128.1
                netmask 255.255.252.0

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.26.144.1
                netmask 255.255.255.0
    ```

    * **Linie**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.26.32.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.26.16.1
                netmask 255.255.254.0

            # Static config for eth2
            auto eth2
            iface eth2 inet static
                address 10.26.8.1
                netmask 255.255.255.252
    ```

    * **Lawine**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.26.8.2
                netmask 255.255.255.252

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.26.0.1
                netmask 255.255.255.192
    ```

    * **Heiter**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
                address 10.26.0.3
                netmask 255.255.255.192

            # Static config for eth1
            auto eth1
            iface eth1 inet static
                address 10.26.4.1
                netmask 255.255.252.0
    ```

 * ### Client
    * **LateKorridor**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.28.64.2
            netmask 255.255.255.224                								 
            gateway 10.28.64.1			
    ```		
    * **LaubHills**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.28.8.2
            netmask 255.255.248.0               							 
            gateway 10.28.8.1										                               
    ```
    * **AppetitRegion**
    ``` 
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.28.8.3
            netmask 255.255.248.0             								             
            gateway 10.28.8.1										                                
    ```
    * **RohrRoad**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.28.24.2
            netmask 255.255.252.0            								             
            gateway 10.28.24.1										                                
    ```
    * **SchwerMountains**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.28.20.2
            netmask 255.255.255.248           								             
            gateway 10.28.20.1										                                
    ```
    * **RoyalCapital**
    ``` 
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.29.128.2
            netmask 255.255.255.0								                              
            gateway 10.29.128.1									                                
    ```
    * **WilleRegion**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.29.128.3
            netmask 255.255.255.0								                              
            gateway 10.29.128.1									                              
    ```
    * **Ritcher**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.64.2
            netmask 255.255.255.248      
            gateway 10.26.64.1										                                      
    ```
    * **Revolte**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.64.3
            netmask 255.255.255.248        								              
            gateway 10.26.64.1										                                
    ```
    * **TurkRegion**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.128.2
            netmask 255.255.252.0								                              
            gateway 10.26.128.1									                                      
    ```
    * **GrobeForest**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.144.2
            netmask 255.255.255.0 								                              
            gateway 10.26.144.1						               		                                
    ```
    * **GranzChannel**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.16.2
            netmask 255.255.254.0       								                            
            gateway 10.26.16.1									                                                          
    ```
    * **BredtRegion**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.0.2
            netmask 255.255.255.192      								              
            gateway 10.26.0.1									                                        
    ```
    * **RiegelCanyon**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.4.3
            netmask 255.255.252.0  								                      
            gateway 10.26.4.1								                                                
    ```
    * **Sein**
    ```
            # Static config for eth0
            auto eth0
            iface eth0 inet static
            address 10.26.4.2
            netmask 255.255.252.0    								                      
            gateway 10.26.4.1					         				                                              
    ```

  ### Routing
    * **Aura**
    ```
            route add -net 10.28.64.0 netmask 255.255.255.224 gw 10.28.128.2			     
            route add -net 10.28.32.0 netmask 255.255.255.252 gw 10.28.128.2		               
            route add -net 10.28.0.0 netmask 255.255.255.252 gw 10.28.128.2			              
            route add -net 10.28.8.0 netmask 255.255.248.0 gw 10.28.128.2				   
            route add -net 10.28.24.0 netmask 255.255.252.0 gw 10.28.128.2			              
            route add -net 10.28.16.0 netmask 255.255.255.252 gw 10.28.128.2		               
            route add -net 10.28.20.0 netmask 255.255.255.248 gw 10.28.128.2			     
            route add -net 10.26.64.0 netmask 255.255.255.248 gw 10.27.0.2			              
            route add -net 10.26.32.0 netmask 255.255.255.252 gw 10.27.0.2 			              
            route add -net 10.26.16.0 netmask 255.255.254.0 gw 10.27.0.2         			   
            route add -net 10.26.8.0 netmask 255.255.255.252 gw 10.27.0.2			                   
            route add -net 10.26.0.0 netmask 255.255.255.192 gw 10.27.0.2		                              
            route add -net 10.26.4.0 netmask 255.255.252.0 gw 10.27.0.2        		                          
            route add -net 10.26.160.0 netmask 255.255.255.252 gw 10.27.0.2			             
            route add -net 10.26.144.0 netmask 255.255.255.0 gw 10.27.0.2				   
            route add -net 10.26.128.0 netmask 255.255.252.0 gw 10.27.0.2		                              
            route add -net 10.26.192.0 netmask 255.255.255.252 gw 10.27.0.2        		                
            route add -net 10.29.128.0 netmask 255.255.255.0 gw 10.29.0.2
    ```
    * **Frieren**
    ```
            route add -net 10.28.0.0 netmask 255.255.255.252 gw 10.28.32.2			              
            route add -net 10.28.8.0 netmask 255.255.248.0 gw 10.28.32.2				   
            route add -net 10.28.24.0 netmask 255.255.252.0 gw 10.28.32.2		                              
            route add -net 10.28.16.0 netmask 255.255.255.252 gw 10.28.32.2	      		                
            route add -net 10.28.20.0 netmask 255.255.255.248 gw 10.28.32.2
    ```
    * **Flamme**
    ```
            route add -net 10.28.8.0 netmask 255.255.248.0 gw 10.28.0.2			                  
            route add -net 10.28.20.0 netmask 255.255.255.248 gw 10.28.16.2	
    ```
    * **Eisen**
    ```
            route add -net 10.26.16.0 netmask 255.255.254.0 gw 10.26.32.2
            route add -net 10.26.8.0 netmask 255.255.255.252 gw 10.26.32.2
            route add -net 10.26.0.0 netmask 255.255.255.192 gw 10.26.32.2
            route add -net 10.26.0.0 netmask 255.255.255.192 gw 10.26.32.2
            route add -net 10.26.144.0 netmask 255.255.255.0 gw 10.26.160.2
            route add -net 10.26.128.0 netmask 255.255.252.0 gw 10.26.160.2
            route add -net 10.29.128.0 netmask 255.255.255.0 gw 10.27.0.1
            route add -net 10.26.4.0 netmask 255.255.252.0 gw 10.26.32.2
    ```
    * **Linie**
    ```
            route add -net 10.26.0.0 netmask 255.255.255.192 gw 10.26.8.2	                                           
            route add -net 10.26.4.0 netmask 255.255.252.0 gw 10.26.8.2
    ```
    * **Lawine**
    ```
            route add -net 10.26.4.0 netmask 255.255.252.0 gw 10.26.0.3   
    ```
  ### Hasil Testing CIDR

https://github.com/laurivasyyy/Jarkom-Modul-4-D09-2023/assets/90681617/bbdd193d-62a6-4005-b694-0cc946a7c4be


