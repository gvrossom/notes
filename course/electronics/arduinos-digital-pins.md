Back to [Electronics101](.)  
Previous: [Discover the tools](./get-to-know-the-tools)  
Next: [Discover the analog pins of the Arduino](./arduinos-analog-pins)
<hr>

The **digital** pins of the Arduino can read only two states: when there is voltage on an input pin, and when there's not. They are somteimes called *binary*, for two states: **HIGH** and **LOW**. *High* means "there is voltage" and *low* "there is no voltage".

We'll use the `digitalWrite()` command to turn it on and off, and `digitalRead()` well, to read it as input.

The digital pins can act as both inputs, such as to listen to a switch, and outputs, such as to control an LED. In the code, we will configure them accordingly.


## Building a spaceship interface - 60 minutes

In this lesson we will discover how to use the *digital* pins of the Arduino.

We will need:

* a switch
* Three LEDs
* Three 220 0hm resistors
* a 10 KILOhm resistor

[Check out the Spacechip Interfase Schematic view]

Here is the accompanying code:

```
int switchState = 0;

void setup(){
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(5, OUTPUT);
  pinMode(2, INPUT);
}

void loop(){
  switchState = digitalRead(2);
  // here a comment
  if (switchState == LOW) {
    // the button is not pressed
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);
  }
  else {
    // the button is pressed
    digitalWrite(3, LOW);
    digitalWrite(4, LOW);
    digitalWrite(5, HIGH);
    delay(250); // wait for a quarter second
    // toggle the leds
    digitalWrite(4, HIGH);
    digitalWrite(5, LOW);
    delay(250); // wait for a quarter second.
  }
} // go back to the beginning of the loop
```