## Step One: Determine the values of 𝑌, 𝑋, 𝑌², 𝑋², dan 𝑋𝑌

• Acidic state (𝑌=4) :

<table><tr><td width="810">
   
   1. Dip the sensor into water containing an acidic solution.
      
   2. Wait for the voltage to stabilize.
      
   3. Please record the voltage value (𝑋) read by the sensor.
      
   4. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   5. Calculate all the values and put them in the table.
   
</td></tr></table><br>

• Neutral state (𝑌=7) :

<table><tr><td width="810">
   
   1. Dip the sensor into neutral water.
      
   2. Wait for the voltage to stabilize.
      
   3. Please record the voltage value (𝑋) read by the sensor.
      
   4. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   5. Calculate all the values and put them in the table.
   
</td></tr></table><br>

• Alkaline state (𝑌=10) :

<table><tr><td width="810">
   
   1. Dip the sensor into water containing an alkaline solution.
      
   2. Wait for the voltage to stabilize.
      
   3. Please record the voltage value (𝑋) read by the sensor.
      
   4. Next, find the value of 𝑌², 𝑋², and 𝑋𝑌.
      
   5. Calculate all the values and put them in the table.
   
</td></tr></table><br>

You can see the calculation example as follows :

<img height="220" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/544cb844-59eb-4ea0-81c3-f5daa0ee3bcf">

<br><br>

## Step Two: Find the value of 𝑎 and 𝑏

The values that have been obtained from the previous stage just need to be entered into the equations 𝑎 and 𝑏. The calculation example is like this :

<img height="450" width="500" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/d2545e57-3307-439e-a362-93e71ffb4097"><br><br>

The value of 𝑎 is 21.84 and the value of 𝑏 is -5.27.

<br><br>

## Step Three: Linear Regression Equation

The values of 𝑎 and 𝑏 can just be entered into the linear regression equation so that it becomes :

<img height="30" width="180" src="https://github.com/devancakra/Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot/assets/54527592/b1ebdeee-7ca4-4dfc-8edd-258a9266d31e"><br><br>

The above equation can be directly used for PH4502C sensor calibration purposes.
