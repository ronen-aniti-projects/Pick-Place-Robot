# Developing a Small Differential Drive Mobile Pick and Place Robot for Color Block Detection and Delivery

## The Overview of the Pick and Place Robot
Hardware, software, objective, motivation. 

## The Architecture of the Robot

### The Finite State Machine Subsystem

### The Perception Subsystems

#### Color Block Tracking Subsystem
Input: Camera image, target color
Output: Bounding box, pivot angle.

Show: Calibration curves for distance, even if not used.

#### Obstacle Avoidance Subsystem

The wall avoidance subsystem.

The block avoidance subsystem.
### The Motion Control Subsystem
Input: Motion Primitive Selection, Primitive Parameter. 
Output: Physical Motion that Approximates the Motion Model Assumptions. 

Show: The motion model dR and dPsi as actions, x, y, psi as state.

### The Localization and Relocalization Subsystem
Input: The Current State Estimate
Output: An Updated State Estimate
Logic: Perform Sonar Scanning to Relocalize the Vehicle when the estimate nears the top right corner of the map.  



Show: The Dead Reckoning Subsystem math. 
Show: The 

### Putting the Pick and Place Robot to the Test

Show: A video from the robot's point of view of a complete run. 