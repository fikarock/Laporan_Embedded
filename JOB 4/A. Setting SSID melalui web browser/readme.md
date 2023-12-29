# A.  Setting SSID dan Password Wi-Fi ESP32 melalui Web Server


### a. Rangkaian dan flowchart
Rangkaian pada percobaan ini adalah sebagai berikut :

![1](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/b0c68dac-6833-4e1e-b1e8-c61813f07cb2)



</br>


### b. Source Code
Kode program : <a href="A.%20Setting%20SSID%20melalui%20web%20browser/4A_Web_Server">di sini</a>

### c. Hasil dan Pembahasan
Pada percobaan A, melakukan pengaturan SSID dan password Wi-Fi pada ESP32 melalui sebuah Web Server. ESP32 akan menampilkan daftar SSID Wi-Fi yang tersedia di serial monitor. Program berupaya untuk terhubung ke jaringan Wi-Fi yang telah disimpan di EEPROM, yang merupakan memori non-volatile. Jika koneksi Wi-Fi tidak berhasil atau tombol fisik pada pin D15 (GPIO15) ditekan, program akan memulai proses konfigurasi sebagai titik akses (Access Point) untuk mengonfigurasi ulang kredensial Wi-Fi. Terdapat beberapa fungsi utama, seperti testWifi(void) yang menguji koneksi Wi-Fi dan melaporkan statusnya, launchWeb(void) yang membuka server web lokal untuk konfigurasi Wi-Fi, setupAP(void) yang menginisialisasi titik akses jika koneksi ke jaringan Wi-Fi tidak dapat dilakukan atau tombol fisik ditekan, dan createWebServer(void) yang membuat halaman web untuk konfigurasi kredensial Wi-Fi, termasuk tombol pemindaian jaringan Wi-Fi dan formulir untuk mengatur SSID serta kata sandi Wi-Fi baru. Implementasi menggunakan library WebServer untuk membuat server web lokal pada port 80.

![1](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/90d8a9bf-db1f-4aad-b66f-fe88727a9fec)

![2](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/7726b4f4-7469-4534-8956-c934cbda5835)

![3](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/23f7e16a-b775-42fa-9f20-e68a666146a6)
