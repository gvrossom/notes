Small motors are used for many applications, from fans to model railroads.
<hr>

To control our motor, we'll use an `IRF520` **transistor**.

[We'll need to check the current to which the motor uses]

### Selecting a motor

Several parameters to consider when choosing a motor:

* the **operating voltage**: This can vary from 3 to more than 12V.
* the **current without load**: the amount of current the motor uses at its operating voltage while spinning freely, without anything connected to the motor's shaft.
* The **stall current**: the amount of current used by the motor when it is trying to turn but cannot because of the load on the motor.
* The **speed at the operating voltage**: The motor's speed in revolutions per minute (RPM).

[What are the specs of the motor in use?]

* We have two DC3V 350mA 14200rpm 1.5-3

### Controlling our motor

To control our motor, we'll use a [[transistor]].

The following hardware is required:

* One small 3 (or 5) V electric motor
* one 1K &Omega; resistor (R1)
* one breadboard
* a separate power source
* connecting wires
* an arduino UNO