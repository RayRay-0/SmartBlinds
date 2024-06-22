# SmartBlinds
## Introduction
The SmartBlinds are an automated version of regular blinds which make it easier and more convenient for people who have blinds to manage them. Using a simple hooking system and a single motor, the blinds automatically lower themselves to their specified length when it's bright and roll up again when it's dark.

## Project Overview
The SmartBlinds consist of:
 1. Arduino Uno: The Arduino board acts as the brains of the system, controlling stepper motors and processing sensor inputs through the photoresistor.
 2. Stepper Motor: If the Arduino is the brain, then the Motor is the brawn. It takes the light inputs and turns the chain of beads attached to the original blinds for you.
 3. 3D print: A 3D printed part is required to hook up the chain of beads to the motor properly, and it helps with turning the chain.
 4. Photoresistor: A photocell or photoresistor is a sensor that changes its resistance when light shines on it and tells our Motor when to start lowering or raising the blinds.
 5. (Optional) Batteries: In case (like ours) the motor's power isn't enough to pull the chain of the blinds, you'll need to attach a battery to it.

If all the components have been linked correctly, the blinds should begin to turn accordingly to the light level around the photoresistor. This system shows how steppermotors can be utilized with light sensors for automation of this mundane task.

## Hardware Requirements
To put together the blinds you'll need the following components:
 1. Arduino Uno Board
 2. Blinds (we used ones by Jysk with a bead chain)
 3. 1 Photoresistor
 4. 1 Stepper Motor (28BYJ-48)
 5. A 3D print
 6. Breadboard
 7. Jumper wires
 8. Power supply
 9. Tape and/or other mounting equipment

 ## Software Requirements
 You'll need the following software:
 1. Arduino IDE
 2. Stepper library (included in Arduino IDE)

## Circuit Diagram

