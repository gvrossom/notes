Back to [Electronics 101](/wiki/course/electronics/)  
Previous: the [digital pins of the Arduino](/wiki/course/electronics/arduinos-digital-pins)  
Next: [Pulse Width Modulation](/wiki/course/electronics/pulse-width-modulation)
<hr>

Discover *analog input* and how to use the *serial monitor*.

While switches and buttons are great, there is a lot more to the physical world than on and off. 
Even though the Arduino is a digital tool, 
we can use it to get information from analog sensors to measure things like temperature or light.  
To that matter, the Arduino has a built-in **Analog-to-Digital Converter** (ADC). 
Analog pins can report back a value between 0 and 1023, [0-1023], which maps to a range from 0 volts to 5 volts.

[Make simple calculation here]

In this lesson, we will use:

* A TMP36 temparature sensor, which outputs a voltage that changes directly proportional to the temperature in degrees Celsius.
* An LED
* A 220 Ohm resistor


Temperatur sensors output a changing voltage depending on the temperatur it senses. 
It has three pins: GND, POWER, and, the OUTPUT variable. 
We will read the output variable to use it turn LEDs on and off.

Finally, we will need to use a tool called a **serial monitor** that enables us to report back results from the microcontroller.

[Check the *Temperature Sensor* related schematic view]

Here is the code of the exercice:

```
const int sensorPin = A0;
const float baselineTemp = 20.0; // we set up a baseline manually

void setup(){
  Serial.begin(9600);  // opens a serial port
  for(int pinNumber = 2; pinNumber<5; pinNumber++){
    pinMode(pinNumber,OUTPUT);
    digitalWrite(pinNumber, LOW);
  }
}

void loop(){
  int sensorVal = analogRead(sensorPin);
  Serial.print("Valeur capteur: ");
  Serial.print(sensorVal);
  
  float voltage = (sensorVal/1024.0)*5.0;
  Serial.print(", Volts: ");
  Serial.print(voltage);
  Serial.print(", degres C: ");
  
  float temperature = (voltage - .5) *100;
  Serial.println(temperature);
  
  if(temperature < baselineTemp){
    digitalWrite(2,LOW);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
  }else if(temperature >= baselineTemp+2 && temperature < baselineTemp+4){
    digitalWrite(2,HIGH);
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
  }else if(temperature >= baselineTemp+4 && temperature < baselineTemp+6){
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,LOW);
  }else if(temperature >= baselineTemp+6){
    digitalWrite(2,HIGH);
    digitalWrite(3,HIGH);
    digitalWrite(4,HIGH);
  }
  delay(1);
}
```