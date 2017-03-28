##Objective
Move robot Rover 20 cm exactly,
turn 90 degrees, repeat 4 times, and return to starting position

##Program

- Open EV3 software application
- Open Action (green)list components:
- add: component Move Steering (set as in exercise 2)
- add in sequence: second component Move Steering
- set On for Degrees, Steering = 90, Power = 100, Degrees = X
- calculate X degrees (short theory lesson here)
- Open Flow Control (yellow) list components:
- add a Loop component to englobe the two Action components
- set on Count, number = 4

- Save project as RoverL1Ex3
- Download program to robot Rover
- Unplug and Run from Robot
- Note results


[[root]]

##Programming construct LOOP
A loop basically repeats a list of actions embeded in loop until it reaches an end condition.
Very useful whenever a repeatable pattern is inserted in program.


##Theory
How to calculate the rotation of wheel in degrees from center of axle?

diagram  W-----*-----W

measure distance between center of axle and wheel, length = L

degree of desired rotation, angle = T

radius of wheel = r

Formulae: d = number of degrees of wheel rotation

d = ( T * L ) / r 