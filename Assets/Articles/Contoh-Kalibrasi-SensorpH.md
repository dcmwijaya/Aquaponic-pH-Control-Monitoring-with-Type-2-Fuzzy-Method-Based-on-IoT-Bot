## Tahap Pertama: Menentukan nilai 𝑌, 𝑋, 𝑌², 𝑋², dan 𝑋𝑌

<img width="840" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/07ecfdf2-beb2-4dc1-aa96-96e1d7c8f168" alt="ph-probe-settings">

<br><br>

Sambungkan ``` probe pH (+) ``` ke ``` probe pH (-) ``` untuk mendapatkan nilai ``` netral (7) ```. Selanjutnya, unggah kode program berikut :

```ino
#define pHpin 35 // GPIO pin 35 is used for pH sensor
int pHValue; // This variable is used to hold the ADC reading value from the sensor
float voltage; // This variable is used to store the voltage reading value from the sensor

void setup(){
   Serial.begin(115200); // Default baudrate for ESP32
   pinMode(pHpin, INPUT); // Initialize the pH sensor pins as input
}

void loop(){
   pHValue = analogRead(pHpin); // Read the sensor ADC
   // 4095 => 12 bit ADC resolution
   // Read the sensor voltage
   voltage = pHValue * (5 / 4095.0); 
   Serial.println(voltage); // Print voltage value to Serial Monitor
   delay(1000); // Delay for 1 second
}
```

<br>

Putar potensiometer hingga output yang diinginkan itu tercapai.

<br><br>

• Keadaan ``` asam (𝑌=4) ``` :

<table><tr><td width="810">
   
   1. Celupkan sensor ke dalam air yang mengandung larutan asam.
      
   2. Tunggu hingga tegangan menjadi stabil.
      
   3. Silakan catat nilai tegangan (𝑋) yang dibaca oleh sensor tersebut.
      
   4. Selanjutnya tinggal mencari nilai 𝑌², 𝑋², dan 𝑋𝑌.
      
   5. Silakan hitung semua nilai dan taruh hasilnya ke dalam tabel.
   
</td></tr></table><br>

• Keadaan ``` netral (𝑌=7) ``` :

<table><tr><td width="810">
   
   1. Celupkan sensor ke dalam air yang netral.
      
   2. Tunggu hingga tegangan menjadi stabil.
      
   3. Silakan catat nilai tegangan (𝑋) yang dibaca oleh sensor tersebut.
      
   4. Selanjutnya tinggal mencari nilai 𝑌², 𝑋², dan 𝑋𝑌.
      
   5. Silakan hitung semua nilai dan taruh hasilnya ke dalam tabel.
   
</td></tr></table><br>

• Keadaan ``` basa (𝑌=10) ``` :

<table><tr><td width="810">
   
   1. Celupkan sensor ke dalam air yang mengandung larutan basa.
      
   2. Tunggu hingga tegangan menjadi stabil.
      
   3. Silakan catat nilai tegangan (𝑋) yang dibaca oleh sensor tersebut.
      
   4. Selanjutnya tinggal mencari nilai 𝑌², 𝑋², dan 𝑋𝑌.
      
   5. Silakan hitung semua nilai dan taruh hasilnya ke dalam tabel.
   
</td></tr></table><br>

Contoh perhitungannya dapat anda lihat sebagai berikut :

<img height="220" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/544cb844-59eb-4ea0-81c3-f5daa0ee3bcf">

<br><br>

## Tahap Kedua: Mencari nilai 𝑎 dan 𝑏

Nilai yang sudah didapat dari tahap sebelumnya tinggal dimasukkan ke dalam persamaan ``` 𝑎 ``` dan ``` 𝑏 ```. Contoh perhitungannya seperti ini :

<img height="450" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/d2545e57-3307-439e-a362-93e71ffb4097"><br><br>

Telah didapatkan ``` nilai 𝑎 ``` sebesar ``` 21,84 ``` dan ``` nilai 𝑏 ``` sebesar ``` -5,27 ```.

<br><br>

## Tahap Ketiga: Persamaan Regresi Linear

``` Nilai 𝑎 ``` dan ```nilai 𝑏 ``` tinggal dimasukkan ke dalam persamaan ``` regresi linear ``` sehingga menjadi :

<img height="30" width="180" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/b1ebdeee-7ca4-4dfc-8edd-258a9266d31e"><br><br>

Persamaan di atas bisa langsung digunakan untuk keperluan kalibrasi ``` sensor PH4502C ```.
