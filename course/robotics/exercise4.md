##Objective
Move robot Rover in straight line, but before hitting wall,
make it turn 90 degrees, and continue in straight line

##Program

- Open EV3 software application
- Open Action (green)list components:
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