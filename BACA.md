[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-Skripsi%20-%2D%20Informatika%20UPN%20Veteran%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)


# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Dokumentasi Skripsi - Informatika UPN Veteran Jatim</strong><br><br>
Proyek ini sangat erat kaitannya dengan teknologi pertanian, dimana alat ini digunakan untuk mengontrol atau memonitoring perubahan pH air setiap saat pada area akuaponik. Sistem akuaponik ini sendiri merupakan sistem budidaya gabungan antara ikan dan sayuran dimana kegiatannya saling menguntungkan. Alat ini dilengkapi dengan sistem pendukung keputusan berupa IT2FL dengan interface berbasis Bot of Things (BoT). Alat ini telah diatur sedemikian rupa agar dapat bekerja secara otomatis, namun juga dapat diperintahkan secara manual.

<br><br>

## Fitur / Kerangka Kerja / Alat
| Media | Deskripsi |
| --- | --- |
| Papan Pengembangan | DOIT ESP32 DEVKIT V1 & Arduino Uno |
| Editor Kode | Arduino IDE |
| Driver | USB-Serial CP210X |
| Platform IoT | io-t.net |
| Protokol IoT | MQTT |
| Arsitektur IoT | 4 Lapisan |
| Telegram | API Bot Telegram |
| Matlab |  Fuzzy Interface System |
| Pustaka Arduino | WiFi, PubSubClient, ESPMQTTClient, OneWire, LiquidCrystal I2C, CTBot, & RTClib |
| Aktuator | Submersible pump aquarium, Pneumatic solenoid valve, & Piezo buzzer |
| Sensor | pH Sensor & RTC (real time clock) |
| Layar | LCD I2C |
| Saklar | Switching power supply, Electrical relay 2 channel, & Saklar bulat |
| Komponen Lainnya | ESP32 baseboard, PCB Dot Matrix, Terminal PCB block screw, Kabel Jumper, Socket female jack DC, & Connector male jack DC  |

<br><br>

## Unduh & Instal
1. Arduino IDE

   ```
   https://www.arduino.cc/en/software
   ```
   <br>

2. USB-Serial CP210X

   ```
   https://bit.ly/CP210X_Driver
   ```

<br><br>

## Persyaratan Proyek
<table>
<tr>
<th width="280">Diagram Piktorial</th>
<th width="280">Desain Prototipe</th>
<th width="280">Desain Wadah Utama</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="Pictorial-Diagram"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174567696-c3737937-dbdd-4608-a6a2-3b9ec0cb81cd.jpg" alt="Prototype-Design"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174568419-f564693e-d35d-4d85-b967-3144d6671bf9.jpg" alt="MainBox-Design"></td>
</tr>
</table>
<table>
<tr>
<th width="280">Sistem Antarmuka Fuzzy IT2FL</th>
<th width="280">Variabel Masukan IT2FL</th>
<th width="280">Variabel Keluaran IT2FL</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174572131-696fcda6-43fb-477b-9579-a0a40d02c1db.jpg" alt="FIS-IT2FL"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174571816-eefdd5de-c0cd-487d-8d68-eea659a313eb.jpg" alt="VarIn-IT2FL"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174571258-5da4e0d1-e788-41a9-9937-1d9c6eaf7ada.jpg" alt="VarOut-IT2FL"></td>
</tr>
</table>

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek dengan cara klik: ``` File ``` -> ``` Open ``` -> ``` PH_IT2FL.ino ```.<br><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE<br><br>
   • Cara: klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut:
   
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```
   
3. ``` Pengaturan Board ``` di Arduino IDE<br><br>
   • Cara: klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` esp32 ```. Kemudian pilih Board dengan mengklik: ``` Tools ``` -> ``` Board ``` -> ``` ESP32 Arduino ``` -> ``` DOIT ESP32 DEVKIT V1 ```.<br><br>Mengenai board Arduino Uno yang ada dalam proyek ini hanya digunakan sebatas regulator tegangan. Jadi pada bagian ini anda tidak perlu melakukan konfigurasi Arduino Uno (cukup hanya berfokus pada ESP32 saja).<br><br>
   
4. ``` Ubah Kecepatan Papan ``` di Arduino IDE<br><br>
   • Cara: klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```.<br><br>
   
5. ``` Instal Pustaka ``` di Arduino IDE<br><br>
   • Cara: unduh semua file zip pustaka. Kemudian tempelkan di: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```.<br><br>

6. ``` Pengaturan Port ``` di Arduino IDE<br><br>
   • Cara: klik ``` Port ``` -> Pilih sesuai dengan port perangkat Anda ``` (Anda dapat melihatnya di Device Manager) ```.<br><br>

7. Ubah ``` Nama WiFi ```, ``` Kata Sandi WiFi ```, dan sebagainya sesuai dengan apa yang Anda gunakan saat ini.<br><br>

8. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

9. Jika tidak ada kesalahan dalam kode program, silakan klik: ``` Upload ```.

<br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
   
4. Membuat akun untuk Platform IoT beserta layanannya.<br><br>
    
5. Jika Anda tidak menerapkan poin 2 dan 3 untuk tujuan pengembangan proyek, tidak masalah, tetapi perlu diketahui bahwa beberapa hal perlu diubah sesuai dengan kebutuhan Anda agar sistem dapat bekerja dengan baik.<br><br>

6. Pastikan semua Things telah dibuat.<br><br>

7. Selamat menikmati [Selesai].

<br><br>

## Sorotan
<table>
<tr>
<th width="280">Produk</th>
<th width="280">Sistem Pendukung Keputusan (SPK) IT2FL</th>
<th width="280">Bot Telegram</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="Product"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL-SPK"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="Telegram-Bot"></td>
</tr>
</table>

<br>
<b>Informasi lebih lanjut:</b> <br><br>
<ul>
   • Skripsi: <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Klik Disini</u></a><br><br>
   • Jurnal tipe SINTA: <a href="https://publikasi.mercubuana.ac.id/index.php/Incomtech/article/view/15453"><u>Klik Disini</u></a><br><br>
   • Jurnal tipe Non SINTA: <a href="https://www.researchgate.net/publication/363660330_SISTEM_KONTROL_PH_UP-DOWN_BERBASIS_NODEMCU32_DENGAN_METODE_ON-OFF_CONTROLLER"><u>Klik Disini</u></a>
</ul>

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta (c) 2020 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
