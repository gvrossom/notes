##Objective
Move robot Rover in straight line, but before hitting wall,
make it turn 90 degrees, and continue in straight line

##Program

- Open EV3 software application
- Open Action (green) list components:
- add: component Move Steering (set to On, steering = 0, power = 50)
- add in parallel: second component Move Steering
- set On for Degrees, Steering = 90, Power = 100, Degrees = X (see Ex3)

- Open Flow Control (yellow) list components:
- add a Switch component
- select Infrared Sensor - Compare - Proximity
- set Compare type = 2, Threshold value = 50
- place Move Steering action component (move forward) in top part of Switch
- place Move Steering action component (turn) in bottom part of Switch

- add a Loop component to englobe the other components, set on Unlimited

- Save project as RoverL1Ex4
- Download program to robot Rover
- Unplug and Run from Robot
- Note results


[[root]]


#Programming construct SWITCH
A Switch is a decision point in program where a test condition is read 
and upon which the result will determine the new direction of program flow.
For example, IF Proximity strength is greater than 50 %, THEN robot is too close to wall 
and should therefore turn, ELSE robot continues directly ahead.

Please notice the construction:
IF condition THEN (true) action ELSE (false) do other action.


##Theory
IR Sensor is an infrared IR sensor, emitting and receiving IR rays.
the IR sensor component can calculate the strength of the returned signal 
and then derived its Proximity. This is not very precise measurement of Proximity
because strength of signal depends on reflectivity of material and angle of contact.
Proximity is therefore a measurement between 0 and 100 as a percentage of original signal returned to receptor.
The second result is the Heading which is the angle the returning signal hits the receptors.
Heading will become important in later exercises in order to determine where is the object relative to robot.