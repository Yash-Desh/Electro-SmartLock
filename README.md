**Course Name: Embedded Systems Lab (R4EC4003P)**

**Date: August-December 2023**


# Electro-SmartLock
A 8051 microcontroller based electronic door locking system

## Table of Contents

- [About the Project](#about-the-project)
    - [Aim](#aim)
    - [Description](#description)
- [Getting Started](#getting-started)
    - [Components](#components)
    - [Software](#software)
    - [Tech Stack](#tech-stack)
- [Theory and Approach](#theory-and-approach)
- [Future Work](#future-work)
- [Contributors](#contributors)
- [Acknowledgements and Resources](#acknowledgements-and-resources)

## About The Project

### Aim

Creating a door locking system based on the 8051 microcontroller involves integrating various components such as a keypad, a motor or solenoid for locking/unlocking, and an LCD display for user interaction.

### Description
The purpose of an electronic lock system is to provide a secure and convenient method of
access control. Electronic locks use electronic components, such as keypads, card readers,
or biometric scanners, to authenticate and authorize individuals before granting entry.
These systems enhance security by allowing for more sophisticated access management,
audit trails, and remote control capabilities. Additionally, electronic lock systems
eliminate the need for traditional physical keys, reducing the risk of unauthorized
duplication and providing a more flexible and adaptable approach to securing spaces.


## Getting Started

### Prerequisites

### Components
- 8051 Microcontroller
- 16*2 Alphanumeric LCD LM016L
- Simple DC Motor
- Interactive Matrix Keypad
- Push Pull 4 channel Driver with Diodes L239D
- 12V Battery

### Software
- [Keil uVision 5](https://www.keil.com/download/)
- [Proteus Software](https://drive.google.com/uc?id=1aQ-QefxwPn7Coc0X_xKwAKFt6r3PQLiD&export=download)
- Video [link](https://www.youtube.com/watch?v=A2KrMkxZQmw) for Proteus


### Tech Stack
- Embedded C
- C++


## Theory and Approach

### 8051 Microcontroller

8051 is one of the first and most popular microcontrollers also known as MCS-51. Intel
introduced it in 1981. Initially, it came out as an N-type metal-oxide-semiconductor
(NMOS) based microcontroller, but later versions were based on complementary
metal-oxide-semiconductor(CMOS) technology. These microcontrollers were named
80C51, where C in the name tells that it is based on CMOS technology. It is an 8-bit
microcontroller which means the data bus is 8-bit. Therefore, it can process 8 bits at a
time. It is used in a wide variety of embedded systems like robotics, remote controls, the
automotive industry, telecom applications, power tools, etc.
![8051](https://github.com/Yash-Desh/Electro-SmartLock/assets/84829056/96d7edfa-be73-4c70-8207-fd56b4cad5f7)

Key Features:
- 4 KB on-chip ROM (Program memory).
- 128 bytes on-chip RAM (Data memory).
- The 8-bit data bus (bidirectional).
- 16-bit address bus (unidirectional).
- Four 8-bit input/output ports.

### Circuit Diagram
![circuit diagram](https://github.com/Yash-Desh/Electro-SmartLock/assets/84829056/246366e1-4025-4216-9f7a-d2fd0555a5e4)


### Operation
![process](https://github.com/Yash-Desh/Electro-SmartLock/assets/84829056/96bf2fd8-877b-47b8-994c-1985e2057474)

1. User will enter the password by using keypad which is interfaced with Port 1 of 8051 Microcontroller.
2. LCD is interfaced with microcontroller on Port 2 by 8 data pins.
3. Motor Driver IC L293D is used for controlling DC motors of 12V rating. It is interfaced with Port 3 of micro controller 8051.
4. RS (Register Select) and EN (Enable) Pins of the LCD are connected to Port 3 and the RW(Read-Write) pin is grounded only for writing purposes on the LCD.
5. A 12V battery is used to energize the DC motor through IC293D.

### Working
1. Password is set 1234 by using programming.
2. If user entered correct password by means of keyboard then LCD will indicate correct and Motor will Rotate to open door.
3. If a user entered an incorrect password then the LCD will display "Incorrect" and the motor will not rotate, eventually the door will not open.


https://github.com/Yash-Desh/Electro-SmartLock/assets/84829056/e59043b6-b7f4-44b0-88d1-233e66c55e49



## Future work
In future iterations of the "8051-based door locking system," we aim to implement several enhancements and refinements to further improve its functionality and usability. 
- Integration of biometric authentication methods such as fingerprint or facial recognition can enhance security and user convenience.
- Incorporating wireless communication protocols such as Bluetooth or Wi-Fi enables remote access and control of the locking system through smartphones or other smart devices.
- Implementing advanced encryption techniques ensures data security and prevents unauthorized access to the system.
- Integrating features for logging access attempts and sending notifications to authorized users enhances system monitoring and accountability.
- Exploring energy-efficient design strategies and incorporating power-saving modes can extend the system's battery life and reduce energy consumption, providing a more sustainable solution for long-term deployment.



## Contributors

- [Yash Deshpande](https://github.com/yashLM705)
- [Pratik Kardile](https://github.com/Aerophile-320)

## Acknowledgements and Resources

- Prof. Panchakshari Awaje, VJTI
- [Keil uVision 5: A Step-by-Step Tutorial for Beginners](https://iies.in/blog/keil-uvision-5-a-step-by-step-tutorial-for-beginners/)
- [8051 Programming Using Keil UVision IDE](https://www.instructables.com/8051-Programming-Using-Keil-UVision-IDE/)
- [Proteus Simulation: Door Lock system using 8051](https://youtu.be/y4k4vlxtGcs?si=JNCQsvCgLSQgB3G3)
- [Programming 8051 using Keil Software](https://www.tutorialspoint.com/programming-8051-using-keil-software)
- [Password Based Door Lock System using 8051 Microcontroller](https://www.electronicshub.org/password-based-door-lock-system-using-8051-microcontroller/)
- [Password-based-doorlock-system-in-8051-microprocessor](https://github.com/kmhmubin/Password-based-doorlock-system-in-8051-microprocessor?tab=readme-ov-file)
- [Password Based Door Lock System Using 8051 Microcontroller](https://circuitdiagrams.in/password-based-door-lock-system/)
