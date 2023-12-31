# JOBSHEET 4 - TRANSMISI DATA MENGGUNAKAN PROTOKOL HTTP DAN MQTT

## Abstrak
<p align="justify">HTTP adalah protokol aplikasi untuk sistem informasi terdistribusi yang fokus pada hypermedia, umumnya digunakan untuk melayani permintaan data pengguna dan mengelola situs web. Sebaliknya, MQTT adalah protokol komunikasi di atas TCP/IP, dirancang untuk komunikasi Machine-to-Machine (M2M). MQTT bersifat open source, ringan, memiliki overhead protokol minimal (2 byte), dan efisien dalam konsumsi daya. Protokol ini umumnya digunakan untuk mentransmisikan data dari Node Sensor ke Server.</p>

<p align="justify">Jobsheet ini bertujuan untuk memahami cara kerja protokol HTTP dan MQTT dalam transmisi data (akuisisi dan kendali) pada Platform IoT Node-Red. Selain itu, jobsheet ini juga bertujuan untuk merancang dan mengkonfigurasi perangkat Internet of Things (IoT) menggunakan protokol HTTP dan MQTT untuk tujuan pemantauan dan kendali melalui Platform IoT Node-Red.</p>

**Sub-job** pada jobsheet ini, antara lain:
1. Setting SSID dan Password Wi-Fi ESP32 melalui Web Server
2. Transmisi Data Menggunakan Protokol HTTP
3. Transmisi Data Menggunakan Protokol MQTT
4. Akuisi Data dan Kendali Perangkat IoT Menggunakan Protokol MQTT
5. Pertanyaan dan Tugas

## Alat dan Bahan
**Alat dan Bahan** yang digunakan dalam praktikum ini, antara lain:
1. ESP32 dan Server Node-Red
2. Breadboard
3. Kabel jumper
4. Sensor DHT 11
5. LED (5)
6. Resistor 330, 1K, 10K Ohm (3)

# A. Setting SSID dan Password Wi-Fi ESP32 melalui Web Server

### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut

![job3a](https://github.com/iamanisaamalia/sistemembedded/assets/147674408/a37af924-187d-41d9-8d78-a6316d5a189b)


### b. Source Code
Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/a.%20Setting%20SSID%20dan%20Password%20Wi-Fi%20ESP32%20melalui%20Web%20Server/JOB_4_A.ino">di sini</a>

### c. Hasil 

https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/3874fd3b-d0b9-4b9d-9ab5-d3d577c6d99e

### d. Pembahasan
ESP32 akan menampilkan daftar SSID Wi-Fi yang dapat diakses pada serial monitor. Program tersebut berusaha untuk menghubungkan ke jaringan WiFi yang telah disimpan dalam EEPROM (memori non-volatil). Jika upaya koneksi WiFi tidak berhasil atau terjadi penekanan tombol fisik pada pin D15 (GPIO15), program akan memulai konfigurasi sebagai titik akses (Access Point) guna melakukan pengaturan ulang WiFi. Hasil dari eksperimen ini adalah mencapai koneksi WiFi kampus dengan sukses.

# B. Transmisi Data Menggunakan Protokol HTTP
## Metode Get
### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut

![WhatsApp Image 2024-01-03 at 14 28 55_e658e36e](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/afc9a6c2-d5d9-49c3-b17e-478941ce97af)

### b. Source Code
Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/b.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/4b_Http_Get/4b_step4/4b_step4.ino">di sini</a>

### c. Hasil 

Serial monitor
![4B_Step4 hasil 1](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/70367b87-6a21-406c-b975-dd27eabb3158)

Debug

![4B_Step4 hasil 2](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/e15aef80-80d5-4a2b-b514-7fd18ffb5c6d)

Dashboard
![4B_Step4 hasil 3](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/551d1bac-baac-4651-8f10-3e54c10a536c)

## Metode Post
### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut

![WhatsApp Image 2024-01-03 at 14 28 55_e658e36e](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/5370634c-3a3b-4f71-be4e-d13be8a2b8e9)

### b. Source Code
Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/b.%20Transmisi%20Data%20Menggunakan%20Protokol%20HTTP/4b_Http_Post/4b_http_post/4b_http_post.ino">di sini</a>

### c. Hasil 

Serial monitor
![4b_http_post_hasil 1](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/716bf2ff-78e6-4805-861a-fa7d8c4295e0)

Debug

![4b_http_post_hasil 2](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/c5db590e-23cd-464a-a98a-575d925f5c59)

Dashboard
![4b_http_post_hasil 3](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/fd516aa8-9a46-4f88-8e15-a4c688fae722)

### d. Pembahasan
Bagian ini menampilkan perbedaan dalam metode penggunaan protokol HTTP. Sebelumnya, digunakan metode GET, namun pada bagian ini beralih menggunakan metode POST. Setelah berhasil mengunggah program, hasil yang muncul adalah sebagai berikut.

# C. Transmisi Data Menggunakan Protokol MQTT

### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut

![WhatsApp Image 2024-01-03 at 14 28 55_e658e36e](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/d976ac67-aac5-4fed-b22f-8c0fbf668476)

### b. Source Code

Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/c.%20Transmisi%20Data%20Menggunakan%20Protokol%20MQTT/job_4c/job_4c.ino">di sini</a>

### c. Hasil

Serial Monitor

![job_4c_hasil 1](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/405c630f-785b-46ac-8ee6-fd4cfb85fe58)

Debug

![job_4c_hasil 2](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/8490e7df-54e4-4738-b10e-9faa18af53c5)

Dashboard
![job_4c_hasil 3](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/a54d02ce-e5da-44c6-afa3-e1b0fc010922)

### d. Pembahasan
Dalam percobaan ini, digunakan protokol MQTT, dan server broker yang dipakai adalah EMQX. EMQX adalah suatu server broker yang dirancang khusus untuk mengelola serta mendukung protokol komunikasi berbasis publikasi-berlangganan, seperti MQTT (Message Queuing Telemetry Transport). Server ini ditujukan untuk mendukung komunikasi efisien antar perangkat dalam jaringan IoT (Internet of Things). Setelah berhasil mengunggah program, data dummy seperti dev_id, level, rainfall, dan flow akan dipublikasikan ke topik flood/node1. Output yang terlihat kemudian adalah sebagai berikut.

# D. Akuisisi Data dan Kendali Perangkat IoT Menggunakan Protokol MQTT.

## 1. Melalui Dashboard Node_red

### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut
![WhatsApp Image 2024-01-03 at 14 28 55_e658e36e](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/94c85ae6-a541-4a81-a11a-3aea2da51887)

### b. Source Code
Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/d.%20Akuisi%20Data%20dan%20Pengendalian/4d_led/4d_led.ino">di sini</a>

### c. Hasil

Serial Monitor
 
Debug
  
Dashboard

Hasil Percobaan

### d. pembahasan
Dalam perocbaan ini, protokol yang tetap digunakan adalah MQTT seperti sebelumnya. Perbedaannya terletak pada penambahan fungsionalitas kontrol LED pada dashboard Node-Red. LED tersebut terhubung ke pin D2 dan dapat diatur untuk menyala atau mati melalui perubahan status tombol switch pada dashboard Node-Red.

## 2. Melalui Dashboard Adafruit.io

### a. Rangkaian
Rangkaian pada percobaan ini adalah sebagai berikut

![WhatsApp Image 2024-01-03 at 14 28 55_e658e36e](https://github.com/ghinazhafirah/EMBEDDED/assets/151806874/33ff05eb-3727-48df-b23c-f51a47d39de5)

### b. Source Code
Kode program dapat dilihat <a href="https://github.com/ghinazhafirah/EMBEDDED/blob/main/JOB%204/d.%20Akuisi%20Data%20dan%20Pengendalian/4d_adafruit/4d_adafruit/4d_adafruit.ino">di sini</a>

### c. Hasil

Serial Monitor

Adafruit Widget

Hasil Percobaan

### d. Pembahasan
Dalam percobaan ini, perbedaannya terletak pada pengaturan nyala LED yang dikendalikan melalui dashboard Adafruit. Langkah-langkahnya termasuk masuk ke situs web io.adafruit.com dan membuat akun terlebih dahulu. Selanjutnya, buatlah widget dashboard sesuai dengan panduan pada jobsheet. Hal krusial di sini adalah menentukan IO USERNAME dan IO KEY dalam program Arduino. IO USERNAME merupakan nama pengguna untuk login, sementara IO KEY adalah kunci API yang digunakan untuk otentikasi dan akses ke layanan Adafruit IO. Kunci IO dapat ditemukan di dasbor Adafruit yang ditandai dengan ikon kunci berwarna kuning. Pastikan juga bahwa feed (umpan) telah dikonfigurasi dengan benar. Setelah semuanya selesai diatur, hasilnya akan terlihat seperti yang ditunjukkan.
