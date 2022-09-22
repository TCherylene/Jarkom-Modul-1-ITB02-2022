# Jarkom-Modul-1-ITB02-2022

Anggota kelompok:

1. Asima P. Y. Tampubolon 5027201009
2. Cherylene Trevina 5027201033
3. Fatih Rian Hibatul Hakim 5027201066

Daftar isi:

* [Nomor 1](#nomor-1)
* [Nomor 2](#nomor-2)
* [Nomor 3](#nomor-3)
* [Nomor 4](#nomor-4)
* [Nomor 5](#nomor-5)
* [Nomor 6](#nomor-6)
* [Nomor 7](#nomor-7)
* [Nomor 8](#nomor-8)
* [Nomor 9](#nomor-9)
* [Nomor 10](#nomor-10)

## Nomor 1

Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!

Penyelesaian:
Filter yang digunakan:
`http.host == monta.if.its.ac.id`

Selanjutnya melakukan Follow TCP Stream dengan klik kanan -> Follow -> TCP Stream.

![nomor 1](images/Nomor%1_1.png)

Setelah itu, muncul window baru seperti gambar berikut. Selanjutnya web-server terletak pada tulisan biru bagian “Server”.

Screenshot hasil:

![nomor 1](images/Nomor%1_2.png)

Oleh karena itu, web server: nginx/1.10.3

## Nomor 2

Ishaq sedang bingung mencari topik TA untuk semester ini, lalu ia datang ke website monta dan menemukan **detail topik** pada website "monta.if.its.ac.id", judul TA apa yang dibuka oleh Ishaq?

Penyelesaian:

Cara mengetahui judul TA yang dibuka Ishaq adalah dengan mencari header yang terdapat tulisan “detailTopik” dan website “monta.if.its.ac.id”.

Filter yang digunakan:

`http contains detailTopik && http.host == monta.if.its.ac.id`

![nomor 2](images/Nomor%2_1.png)

Selanjutnya, kami membuka Full Request URI yang terdapat pada paket tersebut.

![nomor 2](images/Nomor%2_2.png)

Selanjutnya, ditemukan bahwa topik tugas akhir yang dibuka adalah: Evaluasi untuk
kerja User Space Filesystem (FUSE)


## Nomor 3

Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

Penyelesaian:

Filter yang digunakan:
`tcp.dstport == 80`

Screenshot hasil:

![nomor 3](images/Nomor%3.png)

## Nomor 4

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

Penyelesaian:

Untuk mencari source yang berasal dari port 21, dapat menggunakan filter `srcport`. Protokol yang tersedia pada port ini adalah **TCP** sehingga filter yang digunakan:

`tcp.srcport == 21`

Screenshot hasil:

![nomor 4](images/Nomor%204.png)

## Nomor 5

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

Penyelesaian:

Untuk mencari source yang berasal dari port 21, dapat menggunakan filter `srcport`. Pada port 443 (untuk HTTPS), terdapat 2 protokol yang kami temukan, yaitu **TCP** dan **UDP**. Oleh karena itu, filter yang kami gunakan menggunakan logical operator `atau` (`||`). Oleh karena itu, filter menjadi:

`tcp.srcport == 443 || udp.srcport == 443`

Screenshot hasil:

![nomor 5](images/Nomor%205.png)

## Nomor 6

Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id!

Penyelesaian:

Untuk menampilkan paket yang hanya menggunakan nama website/domain, dapat menggunakan filter `http.host`. Oleh karena itu, filter menjadi:

`http.host == lipi.go.id`

Screenshot hasil:

![nomor 6](images/Nomor%206.png)

## Nomor 7

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Penyelesaian:

Cara untuk mencari ip kami (di kali linux): `ifconfig`

IP yang muncul adalah `192.168.19.128` (eth0)

Selanjutnya, pada wireshark ditekan capture filter untuk `eth0`. Selanjutnya, pada display filter, untuk mencari sumber ip tertentu, menggunakan filter `ip.src`. Oleh karena itu, filter yang kami gunakan:

`ip.src == 192.168.19.128`

Screenshot hasil: 

![nomor 7](images/Nomor%207.png)

## Nomor 8

Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.

Penyelesaian:


## Nomor 9

Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.

Penyelesaian:


## Nomor 10

Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!

Penyelesaian:
