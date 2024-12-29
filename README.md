# Robotic_Gripping
###### An example of a custom pneumatic gripper integration to get started with pneumatic actuation on a robotic arm.

![GripperMovement](Pictures/GripperMovment.jpg)

## Overview
This repository contains everyting needed to get on understanding on how to integrate a pneumatic actuator on a robotic arm, in our case the [Universal Robot UR10e](https://www.universal-robots.com/products/ur10-robot/) (or any UR model) through the example of a bespoke and affordable pneumatic gripper.

Included in the repository are:

- Custom Pneumatic Gripper CAD Files: For 3D printing the mountable structure of the gripper,
- Wiring Diagram: Including both pneumatic an electrical wiring information,
- Scripts: Grasshopper toolpath example.

## Note on the Signal Workflow

The workflow begins with the Grasshopper script embedding the extrusion commands (open and closed) into the URP file. This file instructs the UR10e to output a digital voltage signal (0-24V) on the digital ouput 0 of the tool I/O M8 female port (TO0). These signals is directly interpreted by the electronic solenoid valve to balance the airflow between output A (open) and B (closed), ultimately actuating the MHC2-25D pneumatic gripper.

The analog signals can also be overwritten in real-time using the UR Teaching Pendant.

**Grasshopper (Extrusion Command Embeded in URP file/G-Code ) ⟶ UR10e (Digital Output 0-24V) ⟶ Electronic Solenoid Valve (Gate A-B) ⟶ MHC2-25D Pneumatic Gripper (Open-Closed)**

