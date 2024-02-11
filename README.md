[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-Undergraduate%20Thesis%20-%2D%20Informatics%20UPN%20Veteran%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)


# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Undergraduate Thesis Project Documentation (S1) - Informatics UPN Veteran Jatim</strong><br><br>
This project is closely related to agricultural technology, where this tool is used to control or monitor changes in water pH at any time in the aquaponics area. This aquaponic system itself is a combined cultivation system between fish and vegetables where the activities are mutually beneficial. This tool is equipped with a decision support system in the form of IT2FL with a Bot of Things (BoT) based interface. This tool has been set up in such a way as to be able to work automatically, but it can also be commanded manually.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | DOIT ESP32 DEVKIT V1 |
| Supporting Board | Arduino Uno R3 |
| Code Editor | Arduino IDE |
| Application Support | Telegram Bot |
| Driver | USB-Serial CP210X |
| IoT Platform | io-t.net |
| IoT Protocol | MQTT |
| IoT Architecture | 4 Layer |
| Matlab |  Fuzzy Interface System |
| Programming Language | C/C++ |
| Arduino Library | • WiFi<br>• PubSubClient<br>• ESPMQTTClient<br>• OneWire<br>• LiquidCrystal I2C<br>• CTBot<br>• RTClib |
| Actuators | • Submersible pump aquarium (x1)<br>• Pneumatic solenoid valve (x2)<br>• Piezo buzzer (x1) |
| Sensor | • pH Sensor (x1)<br>• RTC (x1) |
| Display | LCD I2C (x1) |
| Experimental Object | • Pakcoy mustard seeds<br>• Dumbo catfish fry |
| Other Components | • Micro USB cable - USB type A (x1)<br>• Jumper cable (1 set)<br>• Switching power supply 12V 1A (x1)<br>• Electrical relay 2 channel (x1)<br>• Round switch (x1)<br>• ESP32 expansion board (x1)<br>• PCB Dot Matrix (x1)<br>• Terminal PCB block screw (x10)<br>• Socket female jack DC (x1)<br>• Connector male jack DC (x3)<br>• Probe Elektroda pH (x1)<br>• Pipes (1 set)<br>• Netpot (1 set)<br>• Rockwool (1 set)<br>• Flannel fabric (1 set)<br>• Water filter (x1)<br>• Glass hubcap (1 set)<br>• Bottle (x2)<br>• Aquarium wheeled placemat (x1)<br>• Aquarium (x1)<br>• Casing box (x1)<br>• Skun (1 set)<br>• Galvanized plate (x1)<br>• Bolts plus (1 set)<br>• Nuts (1 set) |

<br><br>

## Download & Install 
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

## Project Designs
<table>
<tr>
<th width="280">Pictorial Diagram</th>
<th width="280">Prototype Design</th>
<th width="280">Main Box Design</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="Pictorial-Diagram"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/86d03081-632b-415c-9962-f38ba9097039" alt="Prototype-Design"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/6d8c4722-5b95-44ba-b383-404d83377334" alt="MainBox-Design"></td>
</tr>
</table>
<table>
<tr>
<th width="280">Fuzzy Interface System IT2FL</th>
<th width="280">IT2FL Input Variable</th>
<th width="280">IT2FL Output Variable</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/199cbe1c-c49f-4e94-b342-b9d13008293e" alt="FIS-IT2FL"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/8430aa92-e75a-4cfd-9091-40e79430eb54" alt="VarIn-IT2FL"></td>
<td><img src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/b1bd8b70-1bde-40b4-b82d-c1436cf3fc1e" alt="VarOut-IT2FL"></td>
</tr>
</table>

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open the project by clicking ``` File ``` -> ``` Open ``` : 

   <table><tr><td width="840">
   
      ``` PH_IT2FL.ino ```

   </td></tr></table><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE

   <table><tr><td width="840">
      
      Click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link :
      
      ```
      https://dl.espressif.com/dl/package_esp32_index.json
      ```

   </td></tr></table><br>
   
3. ``` Board Setup ``` in Arduino IDE

   <table><tr><td width="840">
      
      • Click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` esp32 ```. 
      
      • Then selecting a Board by clicking: ``` Tools ``` -> ``` Board ``` -> ``` ESP32 Arduino ``` -> ``` DOIT ESP32 DEVKIT V1 ```.

      • ``` Arduino Uno ``` board in this project is only used as a voltage regulator.

      • You don't need to configure the ``` Arduino Uno ``` board, just focus on the ``` ESP32 ```.

   </td></tr></table><br>
   
4. ``` Change the Board Speed ``` in Arduino IDE

   <table><tr><td width="840">
      
      Click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```

   </td></tr></table><br>
   
5. ``` Install Library ``` in Arduino IDE

   <table><tr><td width="840">
      
      Download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```

   </td></tr></table><br>

6. ``` Port Setup ``` in Arduino IDE

   <table><tr><td width="840">
      
      Click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```

   </td></tr></table><br>

7. Change the ``` WiFi Name ```, ``` WiFi Password ```, and so on according to what you are currently using.<br><br>

8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, then please click: ``` Upload ```.<br><br>
    
10. Some things you need to do when using the ``` ESP32 board ``` :

    <table><tr><td width="840">
       
      • ``` Arduino IDE ``` information: ``` Uploading... ``` -> immediately press and hold the ``` BOOT ``` button.

      • ``` Arduino IDE ``` information: ``` Writing at .... (%) ``` -> release the ``` BOOT ``` button.

      • Wait until the message appears: ``` Done Uploading ``` -> ``` The program is directly operated ```.

      • Press the ``` EN (RST) ``` button and then ``` Restart ``` to handle the ``` ESP32 ``` board that cannot process the ``` SC ```.

      • Do not press the ``` BOOT ``` and ``` EN ``` buttons at the same time as this may switch to ``` Upload Firmware ``` mode.

    </td></tr></table><br>

11. If there is still a problem when uploading the program, then try to check the ``` driver ``` / ``` port ``` / ``` others ``` section.

<br><br>

## Io-t.net Setup
1. Getting started with io-t.net :

   <table><tr><td width="840">
      
      • Go to the official website at the following link : <a href="https://io-t.net/">io-t.net</a>.
      
      • If you do not have an account, please <a href="https://i-ot.net/register">Register</a> first -> activate your account via email.
      
      • If you already have an account, please <a href="https://i-ot.net/login">Sign In</a> to be able to access io-t.net services.

   </td></tr></table><br>

2. Create a node :

   <table><tr><td width="840">
      
      • Go to ``` Instance ``` menu -> ``` Set Node ```.
      
      • Then give the node a unique name that you use.

   </td></tr></table><br>

3. Create a device :

   <table><tr><td width="840">
      
      • Go to ``` Devices ``` menu.
      
      • Select ``` Add Devices ``` -> fill in the ``` Client ID ```, ``` Access ```, ``` Topic ``` sections as needed. For example like this :
   
      - ``` Client ID ``` -> ``` Phiotnet_v1 ```.

      - ``` Access ``` -> ``` Publish & Subscribe ```.

      - ``` Topic ``` -> ``` detect ```.

   </td></tr></table>
   
<br><br>

## Telegram Bot Setup
1. Open <a href="https://t.me/botfather">@BotFather</a>.<br><br>

2. Type ``` /newbot ```.<br><br>

3. Type the desired bot name, for example: ``` phiotnet_bot ```.<br><br>

4. Type the desired bot username, for example: ``` phiotnet_bot ```.<br><br>

5. Also do it for bot image settings, bot descriptions, and so on according to your needs.<br><br>

6. Copy ``` your telegram bot API token ``` -> then paste it into the ``` #define BOTtoken "YOUR_API_BOT_TOKEN" ``` section. 

   <table><tr><td width="840">
   For example :<br><br>

   ```
   #define BOTtoken "2006772150:AAE6Fdjk3KbiySkzV6CLbd6ClJDzgTfJ5y0"
   ```
   
   </td></tr></table><br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>

5. Please enjoy [Done].

<br><br>

## Demonstration of Application
Via Telegram: <a href="https://t.me/phiotnet_bot">@phiotnet_bot</a>

<br><br>

## Highlights
<table>
<tr>
<th width="280">Product</th>
<th width="280">IT2FL Decision Support System</th>
<th width="280">Telegram Bot</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="Product"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL-SPK"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="Telegram-Bot"></td>
</tr>
</table>

<br>
<strong>More information:</strong> <br><br>
<table><tr><td width="840">
   • Undergraduate Thesis: <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Click Here</u></a><br><br>
   • SINTA-type journals: <a href="https://publikasi.mercubuana.ac.id/index.php/Incomtech/article/view/15453"><u>Click Here</u></a><br><br>
   • Non SINTA-type journals: <a href="https://www.researchgate.net/publication/363660330_SISTEM_KONTROL_PH_UP-DOWN_BERBASIS_NODEMCU32_DENGAN_METODE_ON-OFF_CONTROLLER"><u>Click Here</u></a>
</td></tr></table>

<br><br>

## Disclaimer
This application has been created by including third-party sources. Third parties here are service providers, whose services are in the form of libraries, frameworks, and others. I thank you very much for the service. It has proven to be very helpful and implementable.

<br><br>

## LICENSE
MIT License - Copyright © 2020 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
