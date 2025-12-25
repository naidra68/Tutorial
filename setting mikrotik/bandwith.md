# 🎨 Setting Bandwith Internet pada Mikrotik

Pastikan sudah melakukan setting atau konfigurasi dasar mikrotik secara tepat dan selesai. Jika sudah terpenuhi, maka bisa melanjutkan pembacaan ini.

## 1️⃣ DHCP SERVER LEASES

Pastikan semua IP address yang tersambung ke dalam Leases ini dibuat secara static, dengan cara klik kanan pada IP Address lalu pilih `Make Static`. Pakai comment untuk memberikan text atau menandai Nama Router-nya.

![Gambar DHCP Server Leases](MIKROTIK/dhcp-server%20leases.png)

## 2️⃣ PEMBAGIAN TRAFFIC BANDWITH

Berikut adalah hasil pembagian Bandwith Internet pada Simple Queues.

![Gambar Simple Queues Mikrotik](MIKROTIK/simple%20queues.png)

Anggap saja, memiliki Internet 60Mbps dan akan dibagi sebanyak 5 rumah dan 1 PC.

## 3️⃣ BUAT PARENT TRAFFIC

Untuk pembagian bandwith, perlu membuat parent-nya dimana IP Address yang dimasukkan sesuai port ethernet pada mikrotik-nya.

Sebagai contoh, untuk traffic rumah-rumah sudah pasti menggunakan port ether3 dimana memiliki IP Address `192.168.20.1/24` dan traffic PC menggunakan port ether2 yang memiliki IP Address `192.168.10.1/24`.

Gunakan network untuk kedua IP Address tersebut, maka yang perlu ditulis adalah `192.168.10.0/24` dan `192.168.20.0/24`

### 1️⃣ All Traffic General

Berikut gambaran untuk setting All Traffic pada tab General.

![Gambar All Traffic General](MIKROTIK/all-trafik-general.png)

### 2️⃣ All Traffic Advanced

Berikut gambaran untuk setting All Traffic pada tab Advanced.

![Gambar All Traffic Advanced](MIKROTIK/all-trafik-advanced.png)

<hr>

### 3️⃣ PC Traffic General

Berikut gambaran untuk setting PC Traffic pada tab General.

![Gambar PC Traffic General](MIKROTIK/pc-trafik-general.png)

### 4️⃣ PC Traffic Advanced

Berikut gambaran untuk setting PC Traffic pada tab Advanced.

![Gambar PC Traffic Advanced](MIKROTIK/pc-trafik-advanced.png)

Setelah membuat parent traffic pada masing-masing network, langkah selanjutnya adalah membuat child traffic nya dimana nanti-nya akan diisi oleh IP Address masing-masing device rumah yang telah dibuat static sebelum-nya.

## 4️⃣ BUAT CHILD TRAFFIC

Masing-masing Parent traffic memiliki Child-nya. Untuk Parent Traffic dengan network `192.168.20.0/24` memiliki child sebanyak 5 device yaitu 5 rumah. Maka dari itu, perlu untuk setting masing-masing device tersebut.

### 1️⃣ Rumah Ardian General

Berikut gambaran untuk setting Rumah Ardian pada tab General.

![Gambar Rumah Ardian General](MIKROTIK/rumah-ardian-general.png)

### 2️⃣ Rumah Ardian Advanced

Berikut gambaran untuk setting Rumah Ardian pada tab Advanced.

![Gambar Rumah Ardian Advanced](MIKROTIK/rumah-ardian-advanced.png)

Untuk Rumah Ardian, di limit internet-nya sampai 20MB.

<hr>

### 3️⃣ Rumah Windi General

Berikut gambaran untuk setting Rumah Windi pada tab General.

![Gambar Rumah Windi General](MIKROTIK/rumah-windi-general.png)

### 4️⃣ Rumah Windi Advanced

Berikut gambaran untuk setting Rumah Windi pada tab Advanced.

![Gambar Rumah Windi Advanced](MIKROTIK/rumah-windi-advanced.png)

Untuk Rumah Windi, di limit internet-nya sampai 10MB.

<hr>

### 5️⃣ Rumah Lala General

Berikut gambaran untuk setting Rumah Lala pada tab General.

![Gambar Rumah Lala General](MIKROTIK/rumah-lala-general.png)

### 6️⃣ Rumah Lala Advanced

Berikut gambaran untuk setting Rumah Lala pada tab Advanced.

![Gambar Rumah Lala Advanced](MIKROTIK/rumah-lala-advanced.png)

Untuk Rumah Lala, di limit internet-nya sampai 10MB.

<hr>

### 7️⃣ Rumah Utama General

Berikut gambaran untuk setting Rumah Utama pada tab General.

![Gambar Rumah Utama General](MIKROTIK/rumah-utama-general.png)

### 8️⃣ Rumah Utama Advanced

Berikut gambaran untuk setting Rumah Utama pada tab Advanced.

![Gambar Rumah Utama Advanced](MIKROTIK/rumah-utama-advanced.png)

Untuk Rumah Utama, di limit internet-nya sampai 10MB.

<hr>

### 9️⃣ Rumah Taqim General

Berikut gambaran untuk setting Rumah Taqim pada tab General.

![Gambar Rumah Taqim General](MIKROTIK/rumah-taqim-general.png)

### 🔟 Rumah Taqim Advanced

Berikut gambaran untuk setting Rumah Taqim pada tab Advanced.

![Gambar Rumah Taqim Advanced](MIKROTIK/rumah-taqim-advanced.png)

Untuk Rumah Taqim, di limit internet-nya sampai 10MB.
<hr>

### 1️⃣1️⃣ PC Utama General

Berikut gambaran untuk setting PC Utama pada tab General.

![Gambar PC Utama General](MIKROTIK/pc-utama-general.png)

### 1️⃣2️⃣ PC Utama Advanced

Berikut gambaran untuk setting PC Utama pada tab Advanced.

![Gambar PC Utama Advanced](MIKROTIK/pc-utama-advanced.png)

Untuk PC Utama, di limit internet-nya sampai 10MB.

Setelah semua Child Traffic ter-konfigurasi, maka yang itu sudah selesai. Selamat telah menyelesaikan setting traffic bandwith mikrotik.