# Developing a Small Differential Drive Mobile Pick and Place Robot for Color Block Detection and Delivery

## The Achievement of the Pick and Place Robot
I have designed a pick and place robot capable of delivering nine colored blocks from scattered locations on the floor to a particular location on the floor without colliding with blocks or walls and within 10 minutes. 

## The Architecture of the Robot System
The robot I have developed comprises a finite state machine subsystem, a perception subsystem, a motion control subsystem, a path planning subsystem, and a navigation subsystem. These subsytems work together.  

### The Finite State Machine Subsystem
Inputs: System State, External Measurements

Outputs: State Transition

Show: State Transition Diagram. 

### The Perception Subsystems
The perception subsystems comprise the color block tracking system and the obstacle avoidance subsystem. The purpose of the system as a whole is to take measurements that are useful to completing the robot's mission. The color block tracking subsystem is meant to identify an appropriate local-area motion plan to the target block. The obstacle avoidance subsystem is meant to steer the robot away from obstacles in its path and also meant to stop it from colliding with walls. 

Show: Picture of the relevant hardware. 

#### Color Block Tracking Subsystem
Input: Camera Image, Target Color Flag

Output: Whether Target Identified in Image, Estimated Pivot Angle to Target.

Action: Pivot

Show: Image showing the array to the target color and the pivot angle. Explain the calibration ratio used. 

#### Obstacle Avoidance Subsystem
The obstacle avoidance subsystem comprises the wall avoidance subsystem and the block avoidance subsystem. 

##### The wall avoidance subsystem.
Input: Sonar Estimation

Output: Wall Infront Flag

Action: Stop Robot

Show: Robot driving to wall but stopping early.

##### The block avoidance subsystem.
Input: Camera Image

Output: Block Danger Flag

Action: Stop the Robot, Pivot Left or Right, Move Forward. 

### The Motion Control Subsystem

Input: Motion Primitive Selection, Primitive Parameter. 

Output: Motion Description Flag

Action: Pivot or Straight Motion

Sensors: Optical Encoders 

Actuators: DC Motors, H-Bridge Motor Driver.

Show: The motion model dR and dPsi as actions, x, y, psi as state.

Show: Picture of the relevant hardware.

### The Path Planning Subsystem
This involves planning a straight line path. Pivot. Move straight. Pivot to avoid obstacles. 
Goal: Target Block or Goal Pose.

### The Navigation Subsystem
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