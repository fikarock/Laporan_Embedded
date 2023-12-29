# D. Akuisi Data dan Kendali Perangkat IoT Menggunakan Protokol MQTT

### a. Rangkaian dan flowchart
Rangkaian pada percobaan ini adalah sebagai berikut : 

Node-RED :

![4 nod](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/24b49bce-8d76-4d73-8e42-e427c4c54980)

ADAFRUIT :

![4 ada](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/96e8836d-d86f-4e9c-8ba3-cf5414807c8b)

</br>


### b. Source Code
Berikut ini adalah Kode program Diatas : 

Node-RED : <a href="/1/1.ino">di sini</a>
ADAFRUIT : <a href="/2/2.ino">di sini</a>

### c. Hasil dan Pembahasan
Percobaan D melibatkan akuisisi data dan kendali perangkat IoT menggunakan protokol MQTT, sebuah konsep di mana perangkat Internet of Things (IoT) mengumpulkan data dan menerima instruksi kendali melalui protokol komunikasi MQTT (Message Queuing Telemetry Transport). Perangkat IoT ini mengumpulkan data dari berbagai sensor atau sumber data lainnya, seperti suhu, kelembaban, atau tingkat cahaya, yang relevan dengan lingkungan atau keperluan aplikasi. Setelah mengumpulkan data, perangkat atau server dapat melakukan berbagai tindakan seperti penyimpanan, analisis, atau pengambilan keputusan.
Fungsi setup_wifi() bertanggung jawab atas inisialisasi koneksi WiFi pada perangkat ESP32, memastikan koneksi ke jaringan WiFi sebelum melakukan koneksi ke server MQTT. Fungsi reconnect() mengatur logika penyambungan ulang ke server MQTT jika terjadi gangguan koneksi. Setelah berhasil terhubung, perangkat akan subscribe ke topik "flood/node1" untuk menerima pesan. Ketika ada pesan masuk dari server MQTT, fungsi callback() akan dipanggil dan pesan tersebut akan dicetak ke Serial Monitor.
Inisialisasi client MQTT terjadi dalam fungsi setup() menggunakan client.setServer() dan client.setCallback(). Pada loop utama (loop()), perangkat terus memanggil fungsi client.loop(), memastikan perangkat dapat terus memproses pesan yang diterima dan menjaga koneksi ke server MQTT jika diperlukan.

