Back to [Electronics101](/wiki/course/electronics) / Making small motions with servos
<hr>

A *servo* (short for servomechanism) contains an electric motor that can be commanded to rotate to a specific angular position. For example, you might use a servo to control the steering of a remote control car, the arm of a robot, etc.

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
Servo myservo

void setup()
{
  my servo.attach(4); // control pin on digital four
}

void loop()
{
  myservo.write(180);
  delay(1000);
  myservo.write(90);
  delay(1000);
  myservo.write(0);
  delay(1000);
}
```