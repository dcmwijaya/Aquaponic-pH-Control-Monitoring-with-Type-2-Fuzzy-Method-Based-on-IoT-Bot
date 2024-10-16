[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/cakraawijaya/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot?logo=Codeforces&logoColor=white&color=%23F7DF1E)
![Project](https://img.shields.io/badge/Project-ESP32-light.svg?style=flat&logo=espressif&logoColor=white&color=%23F7DF1E)
![Type](https://img.shields.io/badge/Type-Undergraduate%20Thesis-light.svg?style=flat&logo=gitbook&logoColor=white&color=%23F7DF1E)

# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Dokumentasi Skripsi - Informatika UPN Veteran Jatim</strong><br><br>
Sistem akuaponik adalah sistem pertanian gabungan antara ikan dengan sayuran yang saling menguntungkan. Di sisi lain, gagal panen juga dapat menjadi kekhawatiran bagi para petani akuaponik karena hal ini dapat terjadi kapan saja. Kegagalan panen dapat dipengaruhi oleh banyak faktor, namun biasanya disebabkan oleh ketidakjelasan pH air yang tinggi di sekitar ruang lingkup budidaya. Para petani akuaponik khawatir jika gagal panen terus berlanjut akan membahayakan ketahanan pangan mereka. Proyek ini dibuat dengan harapan dapat mengatasi masalah pH tersebut. Proyek ini telah dilaksanakan dan memakan waktu kurang lebih 1 tahun. Sistem yang dibuat dapat mengontrol dan memonitoring perubahan pH air setiap saat. Sistem ini berbasis Internet of Things (IoT), dengan menggunakan MQTT sebagai protokol komunikasinya. Sistem ini juga dilengkapi dengan kecerdasan buatan, yang menggunakan IT2FL (Interval Type-2 Fuzzy Logic) sebagai pendukung keputusannya. Selain itu, antarmuka sistem menggunakan Telegram Bot, sehingga memudahkan pengguna untuk berinteraksi.

<br><br>

## Kebutuhan Proyek
| Bagian | Deskripsi |
| --- | --- |
| Papan Pengembangan | DOIT ESP32 DEVKIT V1 |
| Papan Pendukung | Arduino Uno R3 |
| Editor Kode | Arduino IDE |
| Dukungan Aplikasi | • Bot Telegram<br>• Matlab R2020 |
| Driver | CP210X USB Driver |
| Platform IoT | io-t.net |
| Protokol Komunikasi | • Inter Integrated Circuit (I2C)<br>• Message Queuing Telemetry Transport (MQTT)<br>• MTProto |
| Arsitektur IoT | 4 Lapisan |
| Matlab |  Fuzzy Interface System |
| Bahasa Pemrograman | C/C++ |
| Pustaka Arduino | • WiFi (bawaan)<br>• Wire (bawaan)<br>• PubSubClient<br>• LiquidCrystal_I2C<br>• CTBot<br>• ArduinoJson<br>• RTClib |
| Aktuator | • Submersible pump aquarium (x1)<br>• Pneumatic solenoid valve (x2)<br>• Piezoelectric (x1) |
| Sensor | • pH Sensor (x1)<br>• RTC (x1) |
| Layar | LCD I2C (x1) |
| Objek Percobaan | • Benih sawi pakcoy<br>• Benih lele dumbo |
| Komponen Lainnya | • Kabel USB Mikro - USB tipe A (x1)<br>• Kabel jumper (1 set)<br>• Switching power supply 12V 1A (x1)<br>• Electrical relay 2 channel (x1)<br>• Saklar bulat (x1)<br>• Papan ekspansi ESP32 (x1)<br>• PCB Dot Matrix (x1)<br>• Terminal PCB block screw (x10)<br>• Socket female jack DC (x1)<br>• Connector male jack DC (x3)<br>• Probe Elektroda pH (x1)<br>• Pipa (1 set)<br>• Netpot (1 set)<br>• Rockwool (1 set)<br>• Kain flanel (1 set)<br>• Saringan air (x1)<br>• Gelas dop (1 set)<br>• Botol (x2)<br>• Tatakan beroda akuarium (x1)<br>• Akuarium (x1)<br>• Kotak casing (x1)<br>• Skun (1 set)<br>• Plat galvanis (x1)<br>• Baut plus (1 set)<br>• Mur (1 set) |

<br><br>

## Unduh & Instal
1. Arduino IDE

   <table><tr><td width="810">
      
   ```
   https://www.arduino.cc/en/software
   ```

   </td></tr></table><br>

2. CP210X USB Driver

   <table><tr><td width="810">

   ```
   https://bit.ly/CP210X_USB_Driver
   ```

   </td></tr></table><br>

3. Matlab R2020

   <table><tr><td width="810">

   ```
   https://bit.ly/Matlab_R2020a_Installer
   ```

   </td></tr></table>

<br><br>

## Rancangan Proyek
<table>
<tr>
<th width="280">Diagram Ilustrasi</th>
<th width="280">Desain Prototipe</th>
<th width="280">Desain Wadah Utama</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Diagram/Pictorial Diagram.jpg" alt="pictorial-diagram"></td>
<td><img src="Assets/Documentation/Design/Prototype Design.jpg" alt="prototype-design"></td>
<td><img src="Assets/Documentation/Design/Main Box Design.jpg" alt="mainBox-design"></td>
</tr>
</table>
<table>
<tr>
<th width="280">Sistem Antarmuka Fuzzy IT2FL</th>
<th width="280">Variabel Masukan IT2FL</th>
<th width="280">Variabel Keluaran IT2FL</th>
</tr>
<tr>
<td><img src="Assets/Documentation/Experiment/Fuzzy Interface System IT2FL.jpg" alt="fis-it2fl"></td>
<td><img src="Assets/Documentation/Experiment/IT2FL Input Variable.jpg" alt="varin-it2fl"></td>
<td><img src="Assets/Documentation/Experiment/IT2FL Output Variable.jpg" alt="varout-it2fl"></td>
</tr>
</table>

<br><br>

## Memindai Alamat I2C Yang Ada Pada LCD
<table><tr><td width="840">
   
```ino
#include <Wire.h>

void setup() {
  Wire.begin();
  Serial.begin(115200);
  while (!Serial); // Tunggu monitor serial
  Serial.println("\nI2C Scanner");
}

void loop() {
  int nDevices = 0;
  Serial.println("Scanning...");

  for (byte address = 1; address < 127; ++address) {
    // i2c_scanner menggunakan nilai balik dari Wire.endTransmission
    // Untuk melihat apakah sebuah perangkat memang mengakui alamat tersebut
    Wire.beginTransmission(address);
    byte error = Wire.endTransmission();

    if (error == 0) {
      Serial.print("I2C device found at address 0x");
      if (address < 16) {
        Serial.print("0");
      }
      Serial.print(address, HEX);
      Serial.println("  !");

      ++nDevices;
    } else if (error == 4) {
      Serial.print("Unknown error at address 0x");
      if (address < 16) {
        Serial.print("0");
      }
      Serial.println(address, HEX);
    }
  }
  if (nDevices == 0) {
    Serial.println("No I2C devices found\n");
  } else {
    Serial.println("done\n");
  }
  delay(5000); // Tunggu 5 detik untuk pemindaian berikutnya
}
```

</td></tr></table><br><br>

## Kalibrasi Sensor pH
Sensor pH dapat di kalibrasi dengan menggunakan hasil perhitungan regresi linear. Persamaan regresi linear dapat anda lihat sebagai berikut.

<table>
   <tr>
   <td width="40">I</td>
   <td width="800" height="80">

   $\ Y = a+b.X $
         
   </td>
   </tr>
</table><br>

Penjelasan dari simbol-simbol yang ada di persamaan I, dapat anda lihat selengkapnya pada tabel berikut.

<table>
   <tr height="50px">
      <th width="120">Simbol</th>
      <th width="720">Keterangan</th>
   </tr>
   <tr>
      <td>𝑌</td>
      <td>nilai buffer pH</td>
   </tr>
   <tr>
      <td>𝑋</td>
      <td>nilai tegangan yang diperoleh berdasarkan Y</td>
   </tr>
   <tr>
      <td>𝑎 dan 𝑏</td>
      <td>nilai ketetapan regresi linear</td>
   </tr>
</table><br>

Nilai ketetapan regresi linear (a dan b) dapat diperoleh melalui persamaan II dan III.

<table>
   <tr>
   <td width="40">II</td>
   <td width="800" height="80">
   
   $\ a = \frac{\sum Y.\sum X^{2}-\sum X.\sum XY}{n.\sum X^{2}-(\sum X)^{2}} $

   </td>
   </tr>
   <tr>
   <td width="40">III</td>
   <td width="800" height="80">
   
   $\ b = \frac{n.\sum XY-\sum X.\sum Y}{n.\sum X^{2}-(\sum X)^{2}} $

   </td>
   </tr>
</table><br>

Contoh kalibrasi sensor pH: <a href="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/blob/master/Assets/Articles/Contoh-Kalibrasi-SensorpH.md">Klik Disini</a>

<br><br>

## Kalibrasi Sensor RTC
Sensor RTC ini dapat di kalibrasi dengan menggunakan kode program berikut :

<table><tr><td width="840">

```ino
#include <RTClib.h> // Memanggil pustaka RTC
RTC_DS3231 rtc; // Konstruktor

void setup(){
   RTCinit(); // Memanggil metode RTCinit
}

void loop(){}

void RTCinit(){
   // Memulai RTC
   rtc.begin();

   // Pengaturan Tanggal dan Waktu
   rtc.adjust(DateTime(F(__DATE__), F(__TIME__)));

   // Atur Waktu Sekarang
   // Jika sudah di kalibrasi, silakan tutup dengan komentar
   rtc.adjust(DateTime(YYYY,MM,DD,HH,MM,SS));
}
```

</td></tr></table><br><br>

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
   
      • Board ``` Arduino Uno ``` yang ada di proyek ini hanya digunakan sebagai filter atau pembagi tegangan.
   
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

   ```ino
   #define BOTtoken "2006772150:AAE6Fdjk3KbiySkzV6CLbd6ClJDzgTfJ5y0"
   ```

   </td></tr></table>

<br><br>

## Pengaturan Matlab
1. Buka ``` Matlab ```.<br><br>

2. Buka kotak dialog ``` Set Path ``` menggunakan perintah :
   
   <table><tr><td width="810">
      
   ```
   pathtool
   ```

   </td></tr></table>
   
   <img width="810" src="Assets/Documentation/Experiment/MATLAB Set Path.jpg" alt="set-path-matlab"><br><br>

3. Pilih ``` Add Folder... ``` -> cari folder ``` FIS-IT2FLS-Toolbox-MATLAB ``` -> ``` Select Folder ```.<br><br>

4. Klik ``` Save ``` dan kemudian klik ``` Close ```.<br><br>

5. Buka ``` IT2FL Toolbox ``` menggunakan perintah :
   
   <table><tr><td width="810">

   ```
   fuzzyt2
   ```

   </td></tr></table>
   
   <img width="810" src="Assets/Documentation/Experiment/IT2FL Toolbox.jpg" alt="it2fl-toolbox"><br><br>

6. Selebihnya tinggal anda atur sesuai dengan kebutuhan anda.

<br><br>
   
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
<td><img src="Assets/Documentation/Experiment/Product.jpg" alt="product"></td>
<td><img src="Assets/Documentation/Experiment/IT2FL Decision Support System.jpg" alt="it2fl-spk"></td>
<td><img src="Assets/Documentation/Experiment/Telegram Bot.jpg" alt="telegram-bot"></td>
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

## Kekurangan
1. Hardware:

   <table><tr><td width="810">
   
   • Arus bocor listrik disebabkan oleh penggunaan PSU yang tidak standar atau kurangnya isolator yang digunakan.
   
   • Kurangnya sirkulasi udara yang ada di main box dapat menyebabkan panas.
   
   • NO (Normally Open) yang diterapkan pada relay mengakibatkan solenoid valve menjadi panas.
   
   • Kurangnya arus listrik mengakibatkan LCD tidak kuat menyala.
   
   • Penggunaan Arduino Uno sebagai filter atau pembagi tegangan itu dinilai tidak efisien.
   
   • Probe sensor pH tidak memiliki proteksi.
   
   </td></tr></table><br>

2. Firmware:

   <table><tr><td width="810">
   
   • Waktu tunda yang ada di setiap method dinilai berlebihan, seharusnya menggunakan fungsi ``` millis() ``` agar tidak mengganggu method lainnya.

   • Penggunaan ``` io-t.net ``` dinilai kurang maksimal karena diketahui penggunaannya baru sebatas ``` publish ```.

   • Fitur keamanan yang ada pada bot telegram dirasa belum baik.

   </td></tr></table><br>

3. Lainnya:

   <table><tr><td width="810">

   • Pengisian galon pH dan pemberian AB Mix itu masih dilakukan secara manual sehingga menyulitkan pengguna.

   • Pemberian pakan ikan masih dilakukan secara manual.

   • Sawi Pakcoy kurang mendapatkan asupan sinar matahari secara teratur, sehingga setelah pemindahan lahan, perkembangannya tidak secepat sebelumnya.

   • Pengurasan dan pengisian air akuarium ini masih menggunakan cara manual, sehingga sangat merepotkan bagi pengguna.
   
   </td></tr></table>

<br><br>

## Kelebihan  
<table><tr><td width="840">
   
   • Antarmuka sistem melalui bot telegram, sehingga pemberian perintah sekaligus upaya pemantauan dapat dilakukan kapan saja dan dimana saja.
   
   • Dengan IT2FL, akurasi sensor menjadi lebih akurat.

   • Sistem ini secara otomatis dapat mengambil keputusannya sendiri dan juga dapat dikendalikan secara manual oleh pengguna.
   
   • Sistem ini telah dilengkapi dengan fitur pewaktuan.

</td></tr></table><br><br>

## Di Masa Depan
<table><tr><td width="840">
   
   • Perlunya peningkatan arus listrik. Anda dapat menggunakan PSU 3A.
   
   • Perlunya mengubah NO (Normally Open) menjadi NC (Normally Close) pada relay agar perangkat yang dialiri listrik itu dapat terhindar dari kerusakan.

   • Perlunya pembagian tegangan dan arus listrik. Anda dapat menggunakan step down.
   
   • Perlunya peningkatan fitur keamanan pada bot telegram.

   • Perlunya peningkatan keamanan pada sensor pH.
   
   • Perlunya penambahan perangkat re-fill galon pH dan AB mix yang dibuat secara otomatis.
   
   • Perlunya penambahan perangkat yang dapat melakukan pengukuran suhu air dan amonia.
   
   • Perlunya penambahan perangkat dalam pemberian pakan ikan secara otomatis.
   
   • Perlunya penambahan perangkat yang dapat memancarkan sinar hangat sebagai pengganti sinar matahari.
   
   • Perlunya penambahan perangkat yang dapat melakukan pengurasan dan pengisian air akuarium.
   
   • Perlunya penambahan perangkat yang dapat melakukan pendinginan secara optimal pada bagian main box.
   
   • Lahan tanam hidroponik yang ada pada penelitian ini mungkin kedepannya perlu dikembangkan lagi. Selain itu, media tanam rockwool dapat diganti dengan media tanam lain yang lebih mencukupi kebutuhan tanaman, misalnya : arang sekam maupun cocopeat.

</td></tr></table><br><br>

## Apresiasi
Jika karya ini bermanfaat bagi anda, maka dukunglah karya ini sebagai bentuk apresiasi kepada penulis dengan mengklik tombol ``` ⭐Bintang ``` di bagian atas repositori.

<br><br>

## Penafian
Aplikasi ini merupakan hasil karya saya sendiri dan bukan merupakan hasil plagiat dari penelitian atau karya orang lain, kecuali yang berkaitan dengan layanan pihak ketiga yang meliputi: pustaka, kerangka kerja, dan lain sebagainya.

<br><br>

## LISENSI
LISENSI MIT - Hak Cipta © 2022 - Devan C. M. Wijaya, S.Kom

Dengan ini diberikan izin tanpa biaya kepada siapa pun yang mendapatkan salinan perangkat lunak ini dan file dokumentasi terkait perangkat lunak untuk menggunakannya tanpa batasan, termasuk namun tidak terbatas pada hak untuk menggunakan, menyalin, memodifikasi, menggabungkan, mempublikasikan, mendistribusikan, mensublisensikan, dan/atau menjual salinan Perangkat Lunak ini, dan mengizinkan orang yang menerima Perangkat Lunak ini untuk dilengkapi dengan persyaratan berikut:

Pemberitahuan hak cipta di atas dan pemberitahuan izin ini harus menyertai semua salinan atau bagian penting dari Perangkat Lunak.

DALAM HAL APAPUN, PENULIS ATAU PEMEGANG HAK CIPTA DI SINI TETAP MEMILIKI HAK KEPEMILIKAN PENUH. PERANGKAT LUNAK INI DISEDIAKAN SEBAGAIMANA ADANYA, TANPA JAMINAN APAPUN, BAIK TERSURAT MAUPUN TERSIRAT, OLEH KARENA ITU JIKA TERJADI KERUSAKAN, KEHILANGAN, ATAU LAINNYA YANG TIMBUL DARI PENGGUNAAN ATAU URUSAN LAIN DALAM PERANGKAT LUNAK INI, PENULIS ATAU PEMEGANG HAK CIPTA TIDAK BERTANGGUNG JAWAB, KARENA PENGGUNAAN PERANGKAT LUNAK INI TIDAK DIPAKSAKAN SAMA SEKALI, SEHINGGA RISIKO ADALAH MILIK ANDA SENDIRI.
