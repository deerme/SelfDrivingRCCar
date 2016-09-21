# SelfDrivingRCCar
This is the main repository for my next hobby project called "Self Driving RC Car", So, the main objective is to develop a simple prototype to enable autonomous/self driving a rc car (like 1:10 scale) using microservices architecture pattern to run ideally in a Raspberry.

# Principals Projects
## 01 - Simple Racing Car Simulator (in unity3d)
The objetive is design a small simulator that allows driving a car on a circuit (all in 3D), simulating and reporting information such as accelerometer, gyroscopo, GPS, radar, etc. This simulator will export two interfaces.

- TCP/UDP port with information about the car (accelerometer, gyroscope, gps, radar, etc.) and the input for the car controls (left, right, accel, etc.).
- Video Stream in v4l protocolor or similar

In this way, we will use the simulator in a first stage, to make an application that is able to handle autonomously the vehicle on the simulator, directly seeing the video stream (using opencv), reading sensors in order to guide the vehicle by the circuit. The advantage of this decision is that it will develop and implement everything in a simulator environment. Which later will be changed by a real environment (instead of reading the video stream, we will read a real camera on a rc car).

## 02 - Self Driving Engine (c++/python/opencv)
This is the core of the project, this will be the engine of automated driving, and will be a set of services that make the decision to guide the vehicle using information available (video stream and information from GPS, accelerometer, gyro, radar, etc. ). The aim is that this core run on a raspberry.

Sorry for the English (not my mother tongue), but try to keep the entire project flow as understandable as possible according to my level of English xD.
