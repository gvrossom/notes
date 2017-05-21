Back to [Electronics101](.)  
Previous: [pulse width modulation](./pulse-width-modulation)  
Next: [Controlling motors](./controlling-motors)  
<hr>

#### Making small motions with servos

A *servo* (short for servomechanism) contains an electric motor that can be commanded to rotate to a specific angular position. For example, you might use a servo to control the steering of a remote control car, the arm of a robot, etc.

Servos usually only rotate 180 degrees.

### selecting a servo

Several parameters to consider:

* Speed: the time it takes for the servo to rotate, usually measured in seconds per angular degree.
* Rotational range: the angular range through which the servo can rotate - for example, 180 degrees (half of a full rotation) or 360 degrees (one complete rotation).
* Current: How much current the servo draws. When using a servo with an Arduino, you may need to use an external power supply for the servo.
* Torque: The amount of force the servo can exert when rotating. The greater the torque, the heavier the item the servo can control. The torque produced is generally proportional to the amount of current used.

### Connecting a servo

It is easy to connect a servo to an Arduino because only three wires are involved: GND, 5V, and one digital connection; the *pulse* wire.

### Putting a servo to work

Here, the pulse is connected to the digital pin 4:

```
#include <Servo.h>
Servo myservo;
int const potPin = A0;
int potVal;
int angle;

void setup()
{
  my servo.attach(9); // control pin on digital four
  Serial.begin(9600);
}

void loop()
{
  potVal = analogRead(potPin);
  Serial.print("potVal: ");
  Serial.print(potVal);
  
  angle = map(potVal, 0, 1023, 0, 179);
  Serial.print(", angle: ");
  Serial.println(angle);
  myservo.write(angle);
  delay(15);
}
```