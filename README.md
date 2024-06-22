# SmartBlinds
## Introduction
The SmartBlinds are an automated version of regular blinds which make it easier and more convenient for people who have blinds to manage them. Using a simple hooking system and a single motor, the blinds automatically lower themselves to their specified length when it's bright and roll up again when it's dark.

## Project Overview
The SmartBlinds consist of:
 1. Arduino Uno: The Arduino board acts as the brains of the system, controlling stepper motors and processing sensor inputs through the photoresistor.
 2. Stepper Motor: If the Arduino is the brain, then the Motor is the brawn. It takes the light inputs and turns the chain of beads attached to the original blinds for you.
 3. 3D print: A 3D printed part is required to hook up the chain of beads to the motor properly, and it helps with turning the chain.
 4. Control ULN2003: Used to link the Stepper Motor to the Arduino Uno
 5. Photoresistor: A photocell or photoresistor is a sensor that changes its resistance when light shines on it and tells our Motor when to start lowering or raising the blinds.
 6. (Optional) Batteries: In case (like ours) the motor's power isn't enough to pull the chain of the blinds, you'll need to attach a battery to it.

If all the components have been linked correctly, the blinds should begin to turn accordingly to the light level around the photoresistor. This system shows how steppermotors can be utilized with light sensors for automation of this mundane task.

## Hardware Requirements
To put together the blinds you'll need the following components:
 1. Arduino Uno Board
 2. Blinds (we used ones by Jysk with a bead chain)
 3. 1 Photoresistor
 4. 1 Stepper Motor (28BYJ-48)
 5. Contol ULN2003
 6. A 3D print
 7. Breadboard
 8. Jumper wires
 9. Power supply
 10. Tape and/or other mounting equipment

 ## Software Requirements
 You'll need the following software:
 1. Arduino IDE
 2. Stepper library (included in Arduino IDE)

## Circuit Diagram
![circuit](https://github.com/RayRay-0/SmartBlinds/assets/123088926/b5782d13-9438-4bed-a0e3-d7281332977c)

The circuit diagram illustrates the connections between the components.

## Code Explanation
1. The project uses the Stepper library for the clockwise and counter-clockwise movement of the stepper so the blinds can turn
2. We define when it's dark and when it's light
3. And then we define two states, the previous state and current state of the light for the blinds. The default setting has it set to LIGHT.
4. We create two constant int's - one for the steps per revolution for the Stepper, and another for the steps per full rotation. The steps per full rotation are 1000 steps multiplied by however many times it takes for the stepper to turn until the blinds have gone from fully extended to fully rolled up. In our case, it took 17 turns of 1000 steps.
5. We select the node the photoresistor is on and make a number variable for the value of the light level.
6. We set up the stepper with the inputs accordingly. In our case, our inputs were IN1->8, IN2->9, IN3->10, IN4->11.
7. In the setup() we've added a begin and an input at the photoresistor.
8. The methods up() and down() have the speed at which the stepper motor should turn and whether it's turning clockwise or counterclockwise according to how they're mounted to the window.
9. In the loop() secion of our code, we've made the Serial Monitor print the light level, previous and current state of the blinds.
10. The delay in the end is as big as it is so that we can avoid the blinds constantly turning whenever there's lighting.

## Step-by-Step Assembling
1. Connect the Stepper motor to the Arduino Uno board accordingly
2. Assemble the other components on the breadboard and connect accordingly
3. Attach the chain of the blinds to the motor (or 3D printed part attached to the motor)
4. Make sure the chain is fully extended for the most optimal results
5. Put the light sensor/photoresistor somewhere where it can capture the light outside without any obstacles in the way.
6. Upload the code to the Arduino Uno board using Arduino IDE
7. Power the system and adjust the blinds acccordingly.

## Testing and Troubleshooting
The blinds will probably need adjusting, so here's how to test which variables need to be looked for and edited:
1. Mount the blinds and run the code
     - If the blinds don't go in the correct direction, you'll need to change the CW and CCW direction of the up() and down() methods accordingly. (moving the minus (-) from one method to the other until the desired results are met)
2. Count how many times the wheel turns every 1000 steps (or 10,000 steps if the blinds are longer) and change the number the 1000 is multiplied by to the one you counted.
     - This is done to ensure that the blinds turn in one smooth go and don't have to constantly stop. Also to reduce the noise produced by the project.

If you encounter issues like the blinds not turning or turning in the wrong direction/at the wrong time:
1. Check if the chain is being obstructed by anything. There shouldn't be anything in the way of the chain to turn or inside the wheel or the chain.
2. Check if the chain is fully extended. If the chain is too loose, it'll slip off the motor and therefore not turn.
3. Review the code. There's a chance that there's been a syntax error. The first time is never the charm.

## Safery Considerations
While putting together the project make sure your environment is clean.
Works with caution while handling electrical components
Disconnect the circuit from the power source before making any changes

## Conclusion and Future Improvements
The SmartBlinds are an efficient way for regular people, or those with disabilities, to be able to have some privacy without having to worry about constantly going near their windows. They showcase how easily mundane tasks can be automated and one less luxury without the worry about it. 

Possible future improvments for the project:
 - Adding a solar panel so the blinds don't have to rely on the battery
 - Implementing a wireless connection with an app for remote control of the blinds
 - A faster turning motor to cut the time it takes for the blinds to fully lower and rise.

# Who even thought of making this

The best duo team "2 chasa sun" (2-hour sleep)
Dilyara Hristova - purviq chas sun
Raya Ivanova - vtoriq chas sun 
(equally as important)
![logo](https://github.com/RayRay-0/SmartBlinds/assets/123088926/70f7f021-b322-43c7-8838-bfa1b4ab4d0a)
