Back to [Electronics101](/wiki/course/electronics) / 
Next: [Discover the Digital pins of the Arduino](/wiki/course/electronics/arduinos-digital-pins)
<hr>

In this lesson, we will make a simple circuit with some switches, 
an LED, and a resistor.

Electricity is a type of energy, much like:

* Heat
* Gravity
* Light
* ...

Electrical energy flows through **conductors**, like wire. 
You can convert electrical energy into other forms of energy to do something interesting, 
like turn on a light or make some noise out of a speaker.

The components you might use are electrical **transducers**. 
Transducers that turn other type of energy into electrical energy are often called **sensors**, 
and transducers that convert electrical energy into other forms of energy are sometimes called **actuators**.
We build circuits to move electricity through different components.

<hr>

## Electricity Basics

```
Safety Information

! Please never look directly into an LED, since there is a risk of damaging the retina.
! Never connect a polarized capacitor with the plus directly or indirectly to minus of the power supply.
Always check the polarity, before integrating a polarized capacitor in your circuit.
! Please disconnect the power everytime after finishing your experiments.

```

Electric **voltage**  (Unit: Volt "V", or "U") describes the *strength* of the electric field with the charge forced forced to perform a directed movement.
Voltage is the difference in energy between one point in a circuit and another.
It is named after Alessandro Volta, a famous pioneer of physics. He lived in Italy from 1745 to 1827.

Electric **current** (unit: Ampere "A", or "I") is a very abstract concept that describes the flow of electric charges. 
It is a continuous movement of electrical charges (electrons) from the negative pole (anode) to the positive pole (cathode). 
It is named after André-Marie Ampère, a famous French physicist and mathematician, he lived from 1775 to 1836.

Electrical **resistance** (unit: &Omega; Ohm "R") is how much a component resists the flow of electrical energy. 
Resistors are the simplest most frequently used components in electronics.  
It limits the flow of current in a series circuit and divides the voltage in a parrallel circuit.

In a circuit, electricity flows from a point of higher potential energy (usually referred to as power or +) 
to a point of lower potential energy. Ground (often represented with a - or GND) is generally the point of 
least potential energy in a circuit. In the circuits we are building here, electricity only flows in one direction. 
This type of circuits are called  direct current, or DC. 
In Alternating Current (AC) circuits electricity changes its direction 50 or 60 times a second (depending on where you live). 
This is the type of electricity that comes from a wall socket.

### Understanding Ohm's law

**Current, voltage, and resitance are all related.** When you change one of these in a circuit, it affects the others. 
The relationship between them is known as Ohm's law, named for Georg Simon Ohm, who discovered it.

> VOLTAGE (V) = CURRENT (I) * RESISTANCE (R)

Let's build our first circuit using only the `power` source of the Arduino.

We will use:

* A Battery or Power supply. The 5V and ground pins of the Arduino.
* An LED, or Light Emmiting Diode is a component that converts electrical energy into light energy. 
LEDs are polarized components, which means they only allow electricity to flow through them in one direction. 
The longer leg on the LED is called an anode, it will connect to power. The shorter leg is a cathode and will connect to ground.
* A resistor is a component that resists the flow of electrical energy. 
It converts some of the electrical energy into heat. If you put a resistor in series with a component like an LED, 
the resistor will use up some of the electrical energy and the LED will receive less energy as a result. 
This allows you to supply the amount of energy they need. We'll use a resistor in series with the LED to keep it from receiving too much voltage. 
Without it, the LED would be brighter for a few moments, but quickly burn out. 
* A switch interrupts the flow of electricity, breaking the circuit when open. 
When a switch is closed, it will complete a circuit. 
There are many types of switches. The ones we will use here are called momentary switches, 
or pushbuttons, because they are only closed when pressure is applied.

<hr>

## Series and Parallel circuits

Components in *series* come one after another. Components in *parallel* run side by side.

Build a series and a parallel circuit.

<hr>










