## Step One: Determine the values of 𝑌, 𝑋, 𝑌², 𝑋², dan 𝑋𝑌

<img width="810" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/07ecfdf2-beb2-4dc1-aa96-96e1d7c8f168" alt="ph-probe-settings">

<br><br>

Install a jumper cable in the ``` Positive (+) ``` part of the pH BNC connector, then connect it to the ``` Negative (-) ``` part of the pH BNC connector. This was done deliberately by the author to make calibration easier. Next, upload the program code.

<table><tr><td width="810">
   
```ino
#define pHpin 35 // GPIO pin 35 is used for pH sensor
int pHValue; // This variable is used to hold the ADC reading value
float voltage; // This variable is used to store the voltage reading value

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

</td></tr></table><br>

Turn the potentiometer until the desired output is reached (target: 2.5V). This 2.5V is obtained from half of 5V which is assumed to be the value of the neutral voltage determination. If the value has stabilized, then remove the jumper in the pH BNC connector area. Next, perform a test like the following steps :

<br>

• ``` Acidic state (𝑌=4) ```

<table><tr><td width="810">
   
   1. Connect the sensor probe to the BNC connector.
   
   2. Dip the sensor probe into water containing an acidic solution.
      
   3. Wait for the voltage to stabilize.
      
   4. Please record the voltage value (𝑋) read by the sensor.
      
   5. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   6. Calculate all the values and put them in the table.
   
</td></tr></table><br>

• ``` Neutral state (𝑌=7) ```

<table><tr><td width="810">
   
   1. Connect the sensor probe to the BNC connector.
   
   2. Dip the sensor probe into neutral water.
      
   3. Wait for the voltage to stabilize.
      
   4. Please record the voltage value (𝑋) read by the sensor.
      
   5. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   6. Calculate all the values and put them in the table.
   
</td></tr></table><br>

• ``` Alkaline state (𝑌=10) ```

<table><tr><td width="810">
   
   1. Connect the sensor probe to the BNC connector.
   
   2. Dip the sensor probe into water containing an alkaline solution.
      
   3. Wait for the voltage to stabilize.
      
   4. Please record the voltage value (𝑋) read by the sensor.
      
   5. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   6. Calculate all the values and put them in the table.
   
</td></tr></table><br>

You can see the calculation example as follows :

<img height="220" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/544cb844-59eb-4ea0-81c3-f5daa0ee3bcf">

<br><br>

## Step Two: Find the value of 𝑎 and 𝑏

The values that have been obtained from the previous stage just need to be entered into the equations ``` 𝑎 ``` and ``` 𝑏 ```. The calculation example is like this :

<img height="450" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/d2545e57-3307-439e-a362-93e71ffb4097"><br><br>

The ``` value of 𝑎 ``` is ``` 21.84 ``` and the ``` value of 𝑏 ``` is ``` -5.27 ```.

<br><br>

## Step Three: Input 𝑎 and 𝑏 Values in the Linear Regression Equation

The ``` value of 𝑎 ``` and ``` value of 𝑏 ``` can just be entered into the ``` linear regression ``` equation so that it becomes :

<img height="30" width="180" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/b1ebdeee-7ca4-4dfc-8edd-258a9266d31e"><br><br>

The above equation can be directly used for ``` PH4502C sensor ``` calibration purposes.
