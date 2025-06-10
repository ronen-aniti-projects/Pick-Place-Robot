# Developing a Small Differential Drive Mobile Pick and Place Robot for Color Block Detection and Delivery

## The Overview of the Pick and Place Robot
Objective, motivation. 

## The Architecture of the Robot System
State what the robot system comprises (what subsystems). 

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

### The Path Planning Subsystem
This involves planning a straight line path. Pivot. Move straight. Pivot to avoid obstacles. 
Goal: Target Block or Goal Pose.

### The Localization and Relocalization Subsystem
Input: The Current State Estimate
Output: An Updated State Estimate
Logic: Perform Sonar Scanning to Relocalize the Vehicle when the estimate nears the top right corner of the map.  



Show: The Dead Reckoning Subsystem math. 
Show: The 

### Putting the Pick and Place Robot to the Test

#### Integrated Test: Approach of a Block with Obstacles
Test: All three colors. all 4 quadrants relative to start pose. 

Show: Robot point of view camera with ROI and CV2 Put Text for "Target: Red, Pivot Angle: 2 Deg Left, Drawn Bounding Box." Show also trajectory image: Model map image along with estimated actions on map.

#### Integrated Test: Delivery of a Block with Obstacles 

Show: Robot point of view camera with ROI and CV2 put text for "Moving to construction zone; Obstacle detected/not detected; If obstacle detected, then corrective action: Pivoting 5 degrees left...Moving 6 inches forward...Replanning to construction zone".

#### Final Footage

Show: A video from the robot's point of view of a complete run. 