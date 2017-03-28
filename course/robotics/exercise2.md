##Objective
Move robot Rover 20 cm exactly

##Program

- Open EV3 software application
- Action (green) components:
- add: component Move Steering 
- set On for Degrees, Steering = 0, Power = 50, Degrees = X
- calculate X degrees (short theory lesson here)
- Save project as RoverL1Ex2
- Download program to robot Rover
- Unplug and Run from Robot
- Note results

[[root]]



##Theory 
How to measure travel distance of a robot on wheels

1. Calculate Circumference with formulae

	C = 2* Pi* r  	
    
    where C: circumference of wheel, Pi: 3.14159, r: radius of wheel
    
	C value returns value of distance traveled by one rotation of wheel, (unit of radius)

2. Calculate the number of rotations of wheel n for distance x
	
    number of rotations = distance / circumference
    
    n = x / C
    
3. Convert number of rotations to degrees d, 
(remember 1 full wheel rotation = 360 degrees)
	
    number of degrees = number of rotations * 360
    
    d = n * 360

4. Set parameter of motor to rotate by d degrees in a straight line
