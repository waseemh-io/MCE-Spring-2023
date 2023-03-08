# MCE310L - Fundamentals of Mechatronics Engineering Lab
# Assignment #3

<p align="center">Vaughn College of Aeronautics and Technology</p>
<p align="center">Engineering and Technology - Spring 2023</p>
<p align="center">Due Date: Mar 15, 2023</p>

<hr />

## Question #1
Write a function to determine the cost of an automobile insurance premium, based on driver's age and the number of accidents that the driver has had.
The basic insurance charge is $500. There is a surcharge of $100 if the driver is under 25 and an additional surcharge for accidents:
```
# of accidents - accident surcharge
1 			     50
2 			     125
3 			     225
4 			     375
5 			     575
6 or more 	     No insurance
```

This function should be named `calculate_driver_insurance`. It should accept the parameters:
- `age`
- `number of accidents`

The function should return the cost in decimal. If a person does not qualify for insurance it should return the python keyword `None`.

<hr />

## Question #2
Create a class to control a walking robot (think of a boston dynamics robot). This class will connect to a robot and send commands for the robot to follow.

When instantiating an object from this new class, you must pass in the following parameter: 
- `connection_ip_address`
- `name`

**In the constructor you must set an attribute `connected` to False.**
 
This class should have the method: `connect()`. 
This method should verify that you have a valid IP address.
What constitutes a valid IP address? For this problem a IP address is valid if it follows the following convention: `0.0.0.0` . Each digit can be a number from 0-9 and the numbers are separated by a `.`. Examples of other valid IP addresses are:
- `0.1.1.0`
- `1.1.1.9`
- `1.0.3.4`

If it is a valid IP address, print to the terminal "Connected to Robot!" and set the `connected` attribute to True.
If it did not receive a valid IP address, instruct user to set a new IP address.

The next method for this class should be `set_connection_ip_address()`. This method should accept a parameter which is a new IP address and it changes the classes `connection_ip_address` attribute.

Finally the last method should be `move_forward()`. This function should accept the number of steps to move forward
This function should only move forward if the class is connected (HINT: `connected==True`).
If the robot is connected and asked to move forward, then the robot should print every time it takes a step with a 1 second delay each step.
At the end it must print how many stepped it took in that iteration.
ex:
```python
Robocat moved a step forward
Robocat moved a step forward
Robocat moved a step forward
Robocat moved a step forward
Robocat moved 4 steps forward!
Robocat moved a step forward
Robocat moved a step forward
Robocat moved 2 steps forward!
```

If the robot is not connected, instruct user to set a new IP address.

Remember the reason why we like functions and classes. Try to bundle logic/functionality together.
