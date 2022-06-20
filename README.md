[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/Lab-SCR-Informatika-UPN-Veteran-Jatim/IT2FL-Control-Monitoring-pH-Aquaponics-TGBot-IoTBased-ESP32)
![Thesis-Project](https://img.shields.io/badge/Project-S1-%2DInformatika%20UPN%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=008B8B)
![Bot-IoT](https://img.shields.io/badge/Based-IoT-%2DTGBot-%2DIT2FL-light.svg?style=flat&color=008B8B)


# Control-Monitoring-pH-Aquaponics-IoTBased-FuzzyType2
Thesis (S1) Project Documentation - Informatika UPN Veteran Jawa Timur

<br>

## Support Detail
| Media | Penggunaan | Penjelasan |
| --- | --- | --- |
| Broker IoT | Free & Customizable | Platform Internet of Things |
| MCU | DOIT ESP32 DEVKIT V1 | Jenis Mikrokontroler |
| Arduino Lib | WiFi, PubSubClient, ESPMQTTClient, OneWire, LiquidCrystal I2C, CTBot, dan RTClib | Library |
| Telegram | API Bot Telegram | Konfigurasi Bot Telegram |
| Matlab | FIS IT2FL Design | Perancangan & Visualisasi IT2FL |
| Component | pH Sensor, NodeMCU baseboard, Electrical relay 2 channel, Submersible pump aquarium, Pneumatic solenoid valve, Piezo buzzer, LCD I2C, RTC (real time clock), Switching power supply, Arduino Uno, PCB Dot Matrix, Socket female jack DC, Terminal PCB block screw, Kabel jumper, Connector male jack DC, & Saklar bulat | Perangkat Keras |

<br>

## Environment
1. Download Arduino IDE
```bash
https://www.arduino.cc/en/software
```
2. Cantumkan Boards Manager Urls
```bash
https://dl.espressif.com/dl/package_esp32_index.json
```
3. Setting Board di Arduino IDE
   <ul>
      <li>Cara: klik Boards Manager -> ESP32 Arduino -> DOIT ESP32 DEVKIT V1.</li>
   </ul>
4. Setting Port di Arduino IDE
   <ul>
      <li>Cara: klik Port -> Pilihkan sesuai port device anda (dapat anda lihat di device manager).</li>
   </ul>
5. Install Library di Arduino IDE
   <ul>
      <li>Cara: klik Tools -> Manage Libraries -> Install Library sesuai dengan yang ada di tabel Support Detail.</li>
   </ul>

<br>

## Perancangan Hardware
<img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="DesignElectro" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174567696-c3737937-dbdd-4608-a6a2-3b9ec0cb81cd.jpg" alt="DesignAquaponic" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174568419-f564693e-d35d-4d85-b967-3144d6671bf9.jpg" alt="DesignMainBox" width="600" height="400"/>

<br>

## Perancangan Software
<img src="https://user-images.githubusercontent.com/54527592/174572131-696fcda6-43fb-477b-9579-a0a40d02c1db.jpg" alt="FIS_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571816-eefdd5de-c0cd-487d-8d68-eea659a313eb.jpg" alt="VarIn_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571258-5da4e0d1-e788-41a9-9937-1d9c6eaf7ada.jpg" alt="VarOut_IT2FL" width="600" height="400"/>

<br>

## Cara Menerapkan dan Menggunakan Aplikasi
1. Download Repository ini.
2. Pastikan anda memiliki komponen elektronik yang dibutuhkan sesuai tabel Support Detail.
3. Pastikan komponen anda telah dirancang sesuai pada bagian Perancangan Hardware diatas.
4. Pastikan terkoneksi dengan baik (Menyesuaikan settingan Board dan Port).
5. Disarankan untuk membuat akun Broker beserta service nya.
6. Disarankan mengubah code arduino pada bagian Router, Broker, API, dan sebagainya sesuai dengan milik anda.
7. Jika tidak melakukan 2 point diatas (point 2 dan 3) tidak apa-apa *dalam artian: dapat anda kembangkan lagi.
8. Buatlah bot Telegram (tidak disarankan memakai bot telegram yang sudah ada, karena beresiko crash aktivitas).
9. Jika anda merasa kesulitan, terdapat informasi selengkapnya pada bagian paling bawah di keterangan ini.
10. Selesai.

<br>

## Preview: Product
<img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="PreProduct" width="500" height="450"/>

<br>

## Preview: Implementasi Interval Fuzzy Type-2 (SPK)
<img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL" width="500" height="350"/>

<br>

## Preview: Implementasi Bot Telegram (Media Interaktif)
<img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="TGBot" width="500" height="480"/>

<br>

Catatan : Project ini membutuhkan internet dan suplai listrik untuk menjalankan aplikasinya.<br>
<b>Informasi selengkapnya :</b> <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Klik Disini</u></a>
