# C. Transmisi Data Menggunakan Protokol MQTT


### a. Rangkaian dan flowchart
Rangkaian pada percobaan ini adalah sebagai berikut : 

![3](https://github.com/Muhmdwild/Sistem-Embeded/assets/150982519/ff01e0ca-2cf3-48dc-8544-46214b4c1575)

</br>


### b. Source Code
Kode program Diatas : <a href="/1/1.ino">di sini</a>

### c. Hasil dan Pembahasan
Percobaan C, yang melibatkan transmisi data menggunakan protokol MQTT, merupakan suatu metode komunikasi yang efisien dan umumnya digunakan dalam konteks Internet of Things (IoT) serta sistem terdistribusi. MQTT memungkinkan perangkat atau aplikasi untuk berkomunikasi secara andal melalui jaringan yang mungkin memiliki keterbatasan bandwidth atau stabilitas koneksi. Dalam implementasi eksperimen ini, perangkat ESP32 berperan sebagai pengirim data (publisher), menggunakan perintah client.publish() untuk mengirimkan data ke topik yang ditentukan, yaitu "flood/node1". Sementara itu, perangkat penerima data (subscriber) yang tertanam pada server MQTT akan menerima dan memproses data yang dipublikasikan pada topik tersebut.

Fungsi setup_wifi() memiliki tanggung jawab menginisialisasi koneksi WiFi pada perangkat ESP32. Fungsi ini menggunakan SSID dan password WiFi yang telah dikonfigurasi sebelumnya, yang diperlukan agar perangkat dapat terhubung ke jaringan dan berkomunikasi dengan server MQTT. Fungsi reconnect() menangani logika penyambungan ulang (reconnection) ke server MQTT ketika koneksi mengalami gangguan.

Client MQTT diinisialisasi dengan menggunakan fungsi client.setServer() dan diperbarui melalui pemanggilan fungsi client.loop() pada loop utama. Data yang dikirimkan ke server MQTT diformat dalam bentuk JSON menggunakan library ArduinoJson. Informasi seperti dev_id, level, rainfall, dan flow dimasukkan ke dalam objek JSON dan diubah menjadi string JSON. Data yang telah diformat dalam format JSON kemudian dikirimkan ke server MQTT melalui fungsi client.publish("flood/node1", payload), yang bertujuan untuk mempublikasikan data ke topik "flood/node1" pada server MQTT.

