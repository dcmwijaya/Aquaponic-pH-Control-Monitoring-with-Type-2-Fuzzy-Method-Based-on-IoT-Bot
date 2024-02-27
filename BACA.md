[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-Skripsi%20-%2D%20Informatika%20UPN%20Veteran%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)

# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Dokumentasi Skripsi - Informatika UPN Veteran Jatim</strong><br><br>
Sistem akuaponik merupakan sistem budidaya gabungan antara ikan dengan sayuran dimana kegiatannya saling menguntungkan. Di sisi lain, gagal panen juga bisa menjadi kekhawatiran tersendiri bagi para petani akuaponik karena hal ini bisa terjadi sewaktu-sewaktu. Gagal panen bisa dipengaruhi oleh banyak faktor, namun biasanya disebabkan oleh tingginya ambiguitas pH air yang ada di sekitaran ruang lingkup tersebut. Para petani akuaponik khawatir jika gagal panen ini terus berlanjut maka akan berdampak buruk pada ketahanan pangan mereka. Oleh karena itu, proyek ini dibuat pada dasarnya untuk dijadikan sebagai solusi alternatif untuk membantu para petani akuaponik. Proyek ini telah dikerjakan dan memakan waktu selama kurang lebih 1 tahun. Sistem yang dibuat dapat mengontrol sekaligus dapat memonitoring perubahan pH air setiap saat. Sistem yang dibuat ini berbasis Internet of Things (IoT) yaitu dengan menggunakan MQTT sebagai protokol komunikasinya. Sistem ini juga dilengkapi dengan kecerdasan buatan, yaitu memakai IT2FL (Interval Type-2 Fuzzy Logic) sebagai pendukung keputusannya. Selain itu, antarmuka sistem menggunakan Bot Telegram, sehingga dapat memudahkan pengguna dalam berinteraksi.

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | DOIT ESP32 DEVKIT V1 |
| Papan Pendukung | Arduino Uno R3 |
| Editor Kode | Arduino IDE |
| Dukungan Aplikasi | Bot Telegram |
| Driver | USB-Serial CP210X |
| Platform IoT | io-t.net |
| Protokol Komunikasi | • Inter Integrated Circuit (I2C)<br>• Message Queuing Telemetry Transport (MQTT)<br>• MTProto |
| Arsitektur IoT | 4 Lapisan |
| Matlab |  Fuzzy Interface System |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • WiFi (bawaan)<br>• Wire (bawaan)<br>• PubSubClient<br>• LiquidCrystal_I2C<br>• CTBot<br>• ArduinoJson<br>• RTClib |
| Aktuator | • Submersible pump aquarium (x1)<br>• Pneumatic solenoid valve (x2)<br>• Piezo buzzer (x1) |
| Sensor | • pH Sensor (x1)<br>• RTC (x1) |
| Layar | LCD I2C (x1) |
| Objek Percobaan | • Benih sawi pakcoy<br>• Benih lele dumbo |
| Komponen Lainnya | • Kabel Mikro USB - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Switching power supply 12V 1A (x1)<br>• Electrical relay 2 channel (x1)<br>• Saklar bulat (x1)<br>• Papan ekspansi ESP32 (x1)<br>• PCB Dot Matrix (x1)<br>• Terminal PCB block screw (x10)<br>• Socket female jack DC (x1)<br>• Connector male jack DC (x3)<br>• Probe Elektroda pH (x1)<br>• Pipa (1 set)<br>• Netpot (1 set)<br>• Rockwool (1 set)<br>• Kain flanel (1 set)<br>• Saringan air (x1)<br>• Gelas dop (1 set)<br>• Botol (x2)<br>• Tatakan beroda akuarium (x1)<br>• Akuarium (x1)<br>• Kotak casing (x1)<br>• Skun (1 set)<br>• Plat galvanis (x1)<br>• Baut plus (1 set)<br>• Mur (1 set) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   <table><tr><td width="810">
      
   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. USB-Serial CP210X

   <table><tr><td width="810">
      
   ```
   https://bit.ly/CP210X_Driver
   ```

   </td></tr></table>

<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="280">Diagram Piktorial</th>
<th width="280">Desain Prototipe</th>
<th width="280">Desain Wadah Utama</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="Pictorial-Diagram"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/86d03081-632b-415c-9962-f38ba9097039" alt="Prototype-Design"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/6d8c4722-5b95-44ba-b383-404d83377334" alt="MainBox-Design"></td>
</tr>
</table>
<table>
<tr>
<th width="280">Sistem Antarmuka Fuzzy IT2FL</th>
<th width="280">Variabel Masukan IT2FL</th>
<th width="280">Variabel Keluaran IT2FL</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/199cbe1c-c49f-4e94-b342-b9d13008293e" alt="FIS-IT2FL"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/8430aa92-e75a-4cfd-9091-40e79430eb54" alt="VarIn-IT2FL"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/b1bd8b70-1bde-40b4-b82d-c1436cf3fc1e" alt="VarOut-IT2FL"></td>
</tr>
</table>

<br><br>

## Pengaturan Arduino IDE
1. Buka ``` Arduino IDE ``` terlebih dahulu, kemudian buka proyek dengan cara klik ``` File ``` -> ``` Open ``` :

   <table><tr><td width="810">
      
      ``` PH_IT2FL.ino ```

   </td></tr></table><br>
   
2. Isi ``` Url Pengelola Papan Tambahan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` File ``` -> ``` Preferences ``` -> masukkan ``` Boards Manager Url ``` dengan menyalin tautan berikut :
      
      ```
      https://dl.espressif.com/dl/package_esp32_index.json
      ```

   </td></tr></table><br>
   
3. ``` Pengaturan Board ``` di Arduino IDE

   <table>
      <tr><th width="810">

      Cara mengatur board ``` DOIT ESP32 DEVKIT V1 ```
            
      </th></tr>
      <tr><td>
      
      • Klik ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Instal ``` esp32 ```.
   
      • Kemudian klik ``` Tools ``` -> ``` Board ``` -> ``` ESP32 Arduino ``` -> ``` DOIT ESP32 DEVKIT V1 ```.
   
      • Board ``` Arduino Uno ``` yang ada di proyek ini hanya digunakan sebagai regulator tegangan.
   
      • Anda tidak perlu melakukan konfigurasi pada board ``` Arduino Uno ```, cukup hanya berfokus pada ``` ESP32 ``` saja.

      </td></tr>
   </table><br>
   
4. ``` Ubah Kecepatan Papan ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```

   </td></tr></table><br>
   
5. ``` Instal Pustaka ``` di Arduino IDE

   <table><tr><td width="810">
      
      Unduh semua file zip pustaka. Kemudian tempelkan di: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```

   </td></tr></table><br>

6. ``` Pengaturan Port ``` di Arduino IDE

   <table><tr><td width="810">
      
      Klik ``` Port ``` -> Pilih sesuai dengan port perangkat anda ``` (anda dapat melihatnya di Device Manager) ```

   </td></tr></table><br>

7. Ubah ``` Nama WiFi ```, ``` Kata Sandi WiFi ```, dan sebagainya sesuai dengan apa yang anda gunakan saat ini.<br><br>

8. Sebelum mengunggah program, silakan klik: ``` Verify ```.<br><br>

9. Jika tidak ada kesalahan dalam kode program, silakan klik: ``` Upload ```.<br><br>
    
10. Beberapa hal yang perlu anda lakukan saat menggunakan ``` board ESP32 ``` :

    <table><tr><td width="810">
       
       • Informasi ``` Arduino IDE ```: ``` Uploading... ``` -> segera tekan dan tahan tombol ``` BOOT ```.

       • Informasi ``` Arduino IDE ```: ``` Writing at .... (%) ``` -> lepaskan tombol ``` BOOT ```.

       • Tunggu sampai muncul pesan: ``` Done Uploading ``` -> ``` Program langsung dioperasikan ```.

       • Tekan tombol ``` EN (RST) ``` lalu ``` Restart ``` untuk menangani board ``` ESP32 ``` yang tidak bisa memproses ``` SC ```.

       • Jangan tekan tombol ``` BOOT ``` dan ``` EN ``` secara bersamaan karena hal ini bisa beralih ke mode ``` Unggah Firmware ```.

    </td></tr></table><br>

11. Jika masih ada masalah saat unggah program, maka coba periksa pada bagian ``` driver ``` / ``` port ``` / ``` yang lainnya ```.

<br><br>

## Pengaturan io-t.net
1. Memulai io-t.net :

   <table><tr><td width="810">
      
      • Buka situs resminya di tautan berikut : <a href="https://io-t.net/">io-t.net</a>.
      
      • Jika anda belum memiliki akun, silakan <a href="https://i-ot.net/register">Daftar</a> terlebih dahulu -> aktivasi akun melalui email.
      
      • Jika anda sudah memiliki akun, silakan <a href="https://i-ot.net/login">Masuk</a> untuk dapat mengakses layanan io-t.net.

   </td></tr></table><br>

3. Buat node :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Instance ``` -> ``` Atur Node ```.
      
      • Lalu berikan nama yang unik pada node yang anda gunakan.

   </td></tr></table><br>

4. Buat device :

   <table><tr><td width="810">
      
      • Masuk ke menu ``` Devices ```.
   
      • Pilih ``` Tambah Devices ``` -> isi bagian ``` Client ID ```, ``` Access ```, ``` Topic ``` sesuai dengan kebutuhan. Contohnya :
      
      - ``` Client ID ``` -> ``` Phiotnet_v1 ```.
        
      - ``` Access ``` -> ``` Publish & Subscribe ```.
        
      - ``` Topic ``` -> ``` detect ```.

   </td></tr></table>
   
<br><br>

## Pengaturan Bot Telegram
1. Buka <a href="https://t.me/botfather">@BotFather</a>.<br><br>

2. Ketik ``` /newbot ```.<br><br>

3. Ketik nama bot yang diinginkan, contoh: ``` phiotnet_bot ```.<br><br>

4. Ketik nama pengguna bot yang diinginkan, contoh: ``` phiotnet_bot ```.<br><br>

5. Lakukan juga untuk pengaturan gambar bot, deskripsi bot, dan lain sebagainya menyesuaikan dengan kebutuhan anda.<br><br>

6. Salin ``` API token bot telegram anda ``` -> lalu tempelkan pada bagian ``` #define BOTtoken "YOUR_API_BOT_TOKEN" ```. 

   <table><tr><td width="810">
   Contohnya yaitu :<br><br>

   ```
   #define BOTtoken "2006772150:AAE6Fdjk3KbiySkzV6CLbd6ClJDzgTfJ5y0"
   ```

   </td></tr></table><br><br>

## Memulai
1. Unduh dan ekstrak repositori ini.<br><br>
   
2. Pastikan anda memiliki komponen elektronik yang diperlukan.<br><br>
   
3. Pastikan komponen anda telah dirancang sesuai dengan diagram.<br><br>
   
4. Konfigurasikan perangkat anda menurut pengaturan di atas.<br><br>

5. Selamat menikmati [Selesai].

<br><br>

## Demonstrasi Aplikasi
Via Telegram: <a href="https://t.me/phiotnet_bot">@phiotnet_bot</a>

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
<table><tr><td width="840">
      
   • Skripsi: <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Klik Disini</u></a><br><br>
   • Jurnal tipe SINTA: <a href="https://publikasi.mercubuana.ac.id/index.php/Incomtech/article/view/15453"><u>Klik Disini</u></a><br><br>
   • Jurnal tipe Non SINTA: <a href="https://www.researchgate.net/publication/363660330_SISTEM_KONTROL_PH_UP-DOWN_BERBASIS_NODEMCU32_DENGAN_METODE_ON-OFF_CONTROLLER"><u>Klik Disini</u></a>
</td></tr></table>

<br><br>

## Penafian
Aplikasi ini dibuat dengan menyertakan sumber-sumber dari pihak ketiga. Pihak ketiga di sini adalah penyedia layanan, yang layanannya berupa pustaka, kerangka kerja, dan lain-lain. Saya ucapkan terima kasih banyak atas layanannya. Telah terbukti sangat membantu dan dapat diimplementasikan.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2020 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
