[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-S1-%2DInformatika%20UPN%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=008B8B)
![Bot-IoT](https://img.shields.io/badge/Based-IoT-%2DTGBot-%2DIT2FL-light.svg?style=flat&color=008B8B)


# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Undergraduate Thesis Project Documentation (S1) - Informatics UPN Veteran Jatim</strong><br>
This project is closely related to agricultural technology, where this tool is used to control or monitor changes in water pH at any time in the aquaponics area. This aquaponic system itself is a combined cultivation system between fish and vegetables where the activities are mutually beneficial. This tool is equipped with a decision support system in the form of IT2FL with a Bot of Things (BoT) based interface. This tool has been set up in such a way as to be able to work automatically, but it can also be commanded manually.

<br>

## Features / Framework / Tools
| Media | Description |
| --- | --- |
| IoT Platform | io-t.net |
| Board Development | DOIT ESP32 DEVKIT V1 & Arduino Uno |
| Arduino Library | WiFi, PubSubClient, ESPMQTTClient, OneWire, LiquidCrystal I2C, CTBot, & RTClib |
| Telegram | Telegram Bot API |
| Matlab |  Fuzzy Interface System |
| Actuators | Submersible pump aquarium, Pneumatic solenoid valve, & Piezo buzzer |
| Sensor | pH Sensor & RTC (real time clock) |
| Display | LCD I2C |
| Switch | Switching power supply, Electrical relay 2 channel, & Round switch |
| Other Components | ESP32 baseboard, PCB Dot Matrix, Terminal PCB block screw, Jumper cable, Socket female jack DC, & Connector male jack DC  |

<br>

## Download & Install
Download Arduino IDE :
```bash
https://www.arduino.cc/en/software
```

<br>

## Settings
1. Open the Arduino IDE first, then enter the Boards Manager Url by copying the following link:
```bash
https://dl.espressif.com/dl/package_esp32_index.json
```
2. Board Setup in Arduino IDE
   <ul>
      <li>Method: click Boards Manager -> ESP32 Arduino -> DOIT ESP32 DEVKIT V1.</li>
   </ul>
3. Port Setup in Arduino IDE
   <ul>
      <li>Method: click Port -> Choose according to your device port (you can see in device manager).</li>
   </ul>
4. Install Library in Arduino IDE
   <ul>
      <li>Method: click Tools -> Manage Libraries -> Install Library according to project needs.</li>
   </ul>

<br>

## Hardware Design
<img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="DesignElectro" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174567696-c3737937-dbdd-4608-a6a2-3b9ec0cb81cd.jpg" alt="DesignAquaponic" width="600" height="400"/>
<img src="https://user-images.githubusercontent.com/54527592/174568419-f564693e-d35d-4d85-b967-3144d6671bf9.jpg" alt="DesignMainBox" width="600" height="400"/>

<br>

## Software Design
<img src="https://user-images.githubusercontent.com/54527592/174572131-696fcda6-43fb-477b-9579-a0a40d02c1db.jpg" alt="FIS_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571816-eefdd5de-c0cd-487d-8d68-eea659a313eb.jpg" alt="VarIn_IT2FL" width="600" height="300"/>
<img src="https://user-images.githubusercontent.com/54527592/174571258-5da4e0d1-e788-41a9-9937-1d9c6eaf7ada.jpg" alt="VarOut_IT2FL" width="600" height="400"/>

<br>

## Running
1. Download this Repository.
2. Make sure you have the necessary electronic components.
3. Make sure your components have been designed according to the diagram.
4. Make sure the components are well connected (Adjust Board and Port settings).
5. It is recommended to create a Broker account along with this service.
6. Make sure to change the arduino program code in the "Router" section according to the device you are using.
7. If you do not apply points 2 and 3 for the purposes of project development, it is fine, but please note that some things need to be changed in order to function properly.
8. Done, good luck.

<br>

## Preview: Product
<img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="PreProduct" width="500" height="450"/>

<br>

## Preview: Implementation of Fuzzy Interval Type-2 (SPK)
<img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL" width="500" height="350"/>

<br>

## Preview: Telegram Bot Implementation (Interactive Media)
<img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="TGBot" width="500" height="480"/>

<br>

Notes: This project requires internet and electricity supply to run the application.<br>
<b>More information:</b> <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Click Here</u></a>

<br>

## LICENSE
MIT License - Copyright (c) 2023 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
