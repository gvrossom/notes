Back to [Electronics101](/wiki/course/electronics)  
Previous: the [analog pins of the Arduino](/wiki/course/electronics/arduinos-analog-pins)  

<hr>

We know how to make blinking LEDs, but what about fading them, or mixing colors?  
Discover analog output and how to map values.

The Arduino can't vary the output voltage on its pins, it can only output 5V. 
Hence you'll need to use a technique called **Pulse Width Modulation** (PWM) to fade LEDS. 
PWM rapidly turns the output pin high and low over a fixed period of time.  
When you rapidly turn the pin HIGH and LOW, it's as if you changing the voltage. 
The percentage of time a pin is HIGH in a period is called *duty cycle*. 
When the pin is HIGH for half of the period and LOW for the other half, the duty cycle is 50%.

[test to dimmer an LED by setting it to lower]

6 pins set aside for PWM: [Digital pins 3, 5, 6, 9, 10, and 11] identified by the **~**.

[Check out the Fade In Schematic view]

The code for the project:

```
const int greenPin = 9;
const int redPin = 11;
const int bluePin = 10;

const int redSensor = A1;
const int blueSensor = A0;
const int greenSensor = A2;

int redValue = 0;
int blueValue = 0;
int greenValue = 0;

int redSensorValue = 0;
int blueSensorValue = 0;
int greenSensorValue = 0;


void setup() {
  Serial.begin(9600);
  pinMode(greenPin,OUTPUT);
  pinMode(redPin,OUTPUT);
  pinMode(bluePin,OUTPUT);
}

void loop(){
  redSensorValue=analogRead(redSensor);
  delay(5);
  blueSensorValue=analogRead(blueSensor);
  delay(5);
  greenSensorValue=analogRead(greenSensor);
  Serial.print("Raw sensor values \t Red: ");
  Serial.print(redSensorValue);
  Serial.print("\t Green: ");
  Serial.print(greenSensorValue);
  Serial.print("\t Blue: ");
  Serial.println(blueSensorValue);
 
  redValue = redSensorValue/4;
  blueValue = blueSensorValue/4;
  greenValue = greenSensorValue/4;
  
  Serial.print("New values \t Red: ");
  Serial.print(redValue);
  Serial.print("\t Green: ");
  Serial.print(greenValue);
  Serial.print("\t Blue: ");
  Serial.println(blueValue);
  
  analogWrite(redPin, redValue);
  analogWrite(greenPin, greenValue);
  analogWrite(bluePin, blueValue);
}
```