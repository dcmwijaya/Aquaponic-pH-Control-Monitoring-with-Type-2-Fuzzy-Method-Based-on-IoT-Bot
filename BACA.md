[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-S1-%2DInformatika%20UPN%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=008B8B)
![Bot-IoT](https://img.shields.io/badge/Based-IoT-%2DTGBot-%2DIT2FL-light.svg?style=flat&color=008B8B)


# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Dokumentasi Tugas Akhir (S1) - Teknik Informatika UPN Veteran Jatim</strong><br>
Proyek ini sangat erat kaitannya dengan teknologi pertanian, dimana alat ini digunakan untuk mengontrol atau memonitoring perubahan pH air setiap saat pada area akuaponik. Sistem akuaponik ini sendiri merupakan sistem budidaya gabungan antara ikan dan sayuran dimana kegiatannya saling menguntungkan. Alat ini dilengkapi dengan sistem pendukung keputusan berupa IT2FL dengan interface berbasis Bot of Things (BoT). Alat ini telah diatur sedemikian rupa agar dapat bekerja secara otomatis, namun juga dapat diperintahkan secara manual.

<br>

## Fitur / Kerangka Kerja / Alat
| Media | Deskripsi |
| --- | --- |
| Platform IoT | io-t.net |
| Papan Pengembangan | DOIT ESP32 DEVKIT V1 & Arduino Uno |
| Pustaka Arduino | WiFi, PubSubClient, ESPMQTTClient, OneWire, LiquidCrystal I2C, CTBot, & RTClib |
| Telegram | API Bot Telegram |
| Matlab |  Fuzzy Interface System |
| Aktuator | Submersible pump aquarium, Pneumatic solenoid valve, & Piezo buzzer |
| Sensor | pH Sensor & RTC (real time clock) |
| Layar | LCD I2C |
| Saklar | Switching power supply, Electrical relay 2 channel, & Saklar bulat |
| Komponen Lainnya | ESP32 baseboard, PCB Dot Matrix, Terminal PCB block screw, Kabel Jumper, Socket female jack DC, & Connector male jack DC  |

<br>

## Unduh & Instal
Unduh Arduino IDE :
```bash
https://www.arduino.cc/en/software
```

<br>

## Pengaturan
1. Buka Arduino IDE terlebih dahulu, kemudian masukkan Url Boards Manager dengan cara menyalin tautan berikut:
```bash
https://dl.espressif.com/dl/package_esp32_index.json
```
2. Pengaturan Board di Arduino IDE
   <ul>
      <li>Cara: klik Boards Manager -> ESP32 Arduino -> DOIT ESP32 DEVKIT V1.</li>
   </ul>
3. Pengaturan Port di Arduino IDE
   <ul>
      <li>Cara: klik Port -> Pilih sesuai dengan port perangkat Anda (Anda dapat melihatnya di Device Manager).</li>
   </ul>
4. Instal pustaka di Arduino IDE
   <ul>
      <li>Cara: klik Tools -> Manage Libraries -> Instal Pustaka sesuai dengan kebutuhan proyek.</li>
   </ul>

<br>

## Perancangan Perangkat Keras
<img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="DesignElectro" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174567696-c3737937-dbdd-4608-a6a2-3b9ec0cb81cd.jpg" alt="DesignAquaponic" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174568419-f564693e-d35d-4d85-b967-3144d6671bf9.jpg" alt="DesignMainBox" width="600" height="400"/>

<br>

## Perancangan Perangkat Lunak
<img src="https://user-images.githubusercontent.com/54527592/174572131-696fcda6-43fb-477b-9579-a0a40d02c1db.jpg" alt="FIS_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571816-eefdd5de-c0cd-487d-8d68-eea659a313eb.jpg" alt="VarIn_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571258-5da4e0d1-e788-41a9-9937-1d9c6eaf7ada.jpg" alt="VarOut_IT2FL" width="600" height="400"/>

<br>

## Menjalankan
1. Unduh Repositori ini.
2. Pastikan Anda memiliki komponen elektronik yang diperlukan.
3. Pastikan komponen Anda telah dirancang sesuai dengan diagram.
4. Pastikan komponen terhubung dengan baik (Sesuaikan pengaturan Board dan Port).
5. Disarankan untuk membuat akun Broker sekaligus dengan layanannya.
6. Pastikan untuk mengubah kode program arduino di bagian "Router" sesuai dengan perangkat yang Anda gunakan.
7. Jika Anda tidak menerapkan poin 2 dan 3 untuk keperluan pengembangan proyek itu tidak masalah, tetapi harap dicatat bahwa beberapa hal perlu diubah agar dapat berfungsi dengan baik.
8. Selesai, semoga berhasil.

<br>

## Preview: Produk
<img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="PreProduct" width="500" height="450"/>

<br>

## Preview: Implementasi Interval Fuzzy Tipe-2 (SPK)
<img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL" width="500" height="350"/>

<br>

## Preview: Implementasi Bot Telegram (Media Interaktif)
<img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="TGBot" width="500" height="480"/>

<br>

Catatan: Proyek ini membutuhkan internet dan pasokan listrik untuk menjalankan aplikasi.<br><br>
<b>Informasi lebih lanjut:</b> <br>
<ul>
   • Skripsi: <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Click Here</u></a><br>
   • Jurnal tipe SINTA: <a href="https://publikasi.mercubuana.ac.id/index.php/Incomtech/article/view/15453"><u>Click Here</u></a><br>
   • Jurnal tipe Non SINTA: <a href="https://www.researchgate.net/publication/363660330_SISTEM_KONTROL_PH_UP-DOWN_BERBASIS_NODEMCU32_DENGAN_METODE_ON-OFF_CONTROLLER"><u>Click Here</u></a>
</ul>
<br>

## LISENSI
LISENSI MIT - Hak Cipta (c) 2020 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
