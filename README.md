# Internships Portfolio

Welcome to my **Internships Portfolio** repository! This repository contains all the key projects, research work, and implementations I developed during my internships as a student in **Electronics and Communication Engineering (ECE)**.

## Projects

### [EV & ADAS System](./EV&ADAS_project)  
This project focuses on the development of a real-time embedded Electric Vehicle Dashboard with an Ultrasonic Advanced Driver Assistance System (ADAS) Safety Engine. Built on the STM32 "Blue Pill" microcontroller (ARM Cortex-M3 @ 72 MHz) and simulated via PICSimLab, the system models core electric-vehicle behaviour including torque, speed, regenerative braking, and state-of-charge. Alongside the EV dynamics, it features genuine ADAS safety functions—such as Forward Collision Warning, Time-to-Collision estimation, and Blind-Spot Detection—using ultrasonic sensors. A dedicated fault-management layer strictly enforces safe-state behaviour, cutting motor torque instantly upon detecting critical conditions. The complete vehicle state is streamed over UART at 115200 bps to a custom Python Matplotlib dashboard for live, human-readable telemetry visualization. This setup successfully replicates a real-world automotive electronics workflow and hardware-software co-design.
