# B. Basic Flow Transmisi Data Menggunakan Protokol HTTP

Pada percobaan ini Basic Flow atau alur dasar transmisi data menggunakan protokol HTTP mengacu pada urutan langkah-langkah yang terjadi saat klien dan server berkomunikasi melalui protokol Hypertext Transfer Protocol (HTTP).

## 1. Input Dummy Node

### a. Rangkaian
Rangkaian pada percobaan kali ini adalah sebagai berikut.

![langkah-2-1](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/b3d4dce2-9a68-41aa-a704-672487cc54e7)

### b. Hasil dan Pembahasan

![hasil-2-1](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/7ebd2df1-50a5-4200-868f-74d1b9098186)

Output yang dihasilkan adalah Data: "Hello World"

## 2. Parsing Data JSON

### a. Rangkaian
Rangkaian pada percobaan kali ini adalah sebagai berikut.

![langkah-2-2](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/16715349-f168-499e-8cb3-e622b16cbb95)

### b. Hasil dan Pembahasan

![hasil-2-2](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/fb4fe466-8159-43a7-b778-58ca11706d3c)

Output yang dihasilkan adalah 3 data, yaitu temp, humi, dan light yang ditampilkan dalam 3 log berbeda.

## 3. HTTP Response

### a. Rangkaian
Rangkaian pada percobaan kali ini adalah sebagai berikut.

![langkah-2-3](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/1f264173-f893-4ed7-b99e-d1b177c221a6)

### b. Hasil dan Pembahasan

#### OK Response

![hasil-2-3-ok-post](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/4d4ec4ff-2905-4adb-8700-0eff92defb8b)

![hasil-2-3-ok-debug](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/36518d4d-6e67-4c8d-90e1-e8368dde8bd1)

#### Bad Response

![hasil-2-3-bad-post](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/a297a4ea-a112-4e3c-b5ae-72244150bae9)

![hasil-2-3-bad-debug](https://github.com/farhanhisyam/sistemEmbedded/assets/94108385/9c56fdc8-4a5e-4386-bdfe-5888d7b9403d)
