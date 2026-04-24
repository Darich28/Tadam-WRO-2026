  Future Engineers 2026
  ====
  Team name: Tadam
  ==
  <img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/2570ee8e-a9ab-41df-b66a-fc46680e45b8" />

  Team members: Tursynova Dariya, Mukiyanova Alima
  ====
## Content

!['Our team photos'](t-photos) 
-------
* `Our team photos` Meet the team: photos included in this file.
-------
!['Vehicle photos'](v-photos)
-------
* `Vehicle photos` Vehicle photos: Full 360-degree views of our self-driving car.
  
!['Video'](video) 
-------
* `Video` This section contains links to videos demonstrating our robot in motion and providing a detailed explanation of its functions.
-------

!['src'](src) 
-------
* `src` This section includes the algorithms and scripts responsible for the robot's mobility.
-------
!['schemes'](schemes)
-------
* `schemes` This file contains photos of our sensors and motors, steering diagrams, and other detailed technical information about the vehicle.
-------
## Introduction

Our robot is built on the LEGO EV3 platform and is designed for autonomous navigation in the Future Engineers competition.
Hardware Overview

The vehicle consists of the following main components:
EV3 Intelligent Brick – the main controller that processes all data and runs the program.
EV3 Rechargeable Battery – provides power to the entire system.
Drive System:
Two medium motors connected through a gear system and differential, powering the rear wheels (rear-wheel drive).
Steering System:
One medium motor controlling the front wheels using Ackermann steering geometry for smoother and more realistic turning.
Sensors:
Two ultrasonic sensors mounted at the front sides of the robot for obstacle detection and wall tracking.
One gyro sensor placed in the center of the robot for orientation and angle correction.
Software Structure
The control software is organized into several logical modules:
Movement Module
Controls forward motion, speed regulation, and stopping.
Steering Module
Handles turning using the Ackermann steering system and adjusts angles based on sensor input.
Sensor Module
Reads and processes data from ultrasonic and gyro sensors.
Navigation Module
Combines sensor data and movement logic to follow the track, handle turns, and avoid obstacles.

How It Works
The robot starts moving forward using the rear-wheel drive system.
Ultrasonic sensors continuously measure the distance to walls/obstacles.
<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/cdc34a6c-c180-40af-be0f-f3873f82f916" />

The robot adjusts its position to stay aligned with the track.
Before turns, the robot calculates the angle using sensor data.
The steering motor turns the front wheels accordingly.
The gyro sensor helps correct orientation and stabilize movement after turns.
Build and Upload Process
The code is written in the EV3 programming environment (Clev3r / EV3-compatible environment).
The robot is connected to a computer via USB/Bluetooth.
The program is compiled and uploaded directly to the EV3 brick.
After uploading, the program is executed on the EV3 brick.



##  Mobility and Mechanical Design


Our robot uses rear-wheel drive with a differential and an Ackermann steering system. We chose this design because it allows smoother and more accurate turns. The differential helps the wheels rotate at different speeds during turns, which reduces slipping. Ackermann steering improves the turning trajectory, especially on tight corners.

We also tested a tank drive system, but it was less stable and caused more errors due to slipping, so we decided not to use it.

The main trade-off is that Ackermann steering is harder to build and requires careful calibration. However, it gives better control and consistency.

We tested different speeds and turning angles to improve alignment before turns and reduce mistakes during navigation.

Power and Sensor Architecture

Our robot uses two ultrasonic sensors placed at the front sides and one gyro sensor in the center.

The side placement of ultrasonic sensors helps detect walls earlier and adjust the path in advance. The gyro sensor is placed in the center to reduce noise and improve accuracy.

We tried to balance accuracy and energy consumption. Adding more sensors could improve precision, but it would also increase power usage and processing delay.

We calibrate the gyro before each run and apply simple filtering to ultrasonic data to reduce noise.

If one sensor gives unstable readings, the robot relies on the other sensors to maintain stable behavior.

Software Architecture and Strategy

The program is divided into simple modules: movement control, sensor processing, and decision-making.

We use a state-based approach:

moving forward
preparing for a turn
turning
realigning
This makes the robot’s behavior easier to understand and debug.

We also considered edge cases, such as incorrect sensor readings or sudden obstacles.

To evaluate performance, we focused on:

number of successful laps in a row
turning accuracy
lap time
⸻

Systems Thinking and Engineering Decisions

We treated the robot as a connected system where mechanics, sensors, and code all affect each other.

For example, mechanical design affects how accurate the sensors are, and sensor accuracy affects the control algorithm.

We made decisions based on stability rather than maximum speed.

Some risks we identified include gyro drift, ultrasonic delay, and accumulated error over time.

To reduce these risks, we use calibration, simple filtering, and limit extreme movements.

