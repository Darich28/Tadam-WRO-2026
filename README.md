  Future Engineers 2026
  ====
  Team name: Tadam
  ==
  Team members: Tursynova Dariya, Mukiyanova Alima
  ====
## Content

!['Our team photos'](t-photos) 
-------
* `Our team photos` Meet the team: photos included in this file.
-------
!['Vehicle photos'](video)
* `Vehicle photos` Vehicle photos: Full 360-degree views of our self-driving car.
  
!['Video'](video) 
-------

!['Vehicle photos'](video)
* `Vehicle photos` Vehicle photos: Full 360-degree views of our self-driving car.
* `Video` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.

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
The robot adjusts its position to stay aligned with the track.
Before turns, the robot calculates the angle using sensor data.
The steering motor turns the front wheels accordingly.
The gyro sensor helps correct orientation and stabilize movement after turns.
Build and Upload Process
The code is written in the EV3 programming environment (Clev3r / EV3-compatible environment).
The robot is connected to a computer via USB/Bluetooth.
The program is compiled and uploaded directly to the EV3 brick.
After uploading, the program is executed on the EV3 brick.


