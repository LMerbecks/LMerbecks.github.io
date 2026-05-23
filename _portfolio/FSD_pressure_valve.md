---
title: "Blimp UAV Hull Pressure Control System"
excerpt: "Circular MIL-DTL-D38999 connectors are electrical connectors for rugged environments. Their design is scoop proof, contains polarization and separated electrical and mechanical connections. Due to high cost, use of these connectors in non-professional environments is low to non-existent. In this project a version of these connectors is developed that uses additive manufacturing and commonly available stamped electrical contacts to achieve a cost below 1€ for the smallest connector system.<br/><img src='/images/D389993MF/38999_cover.jpeg'>"
collection: portfolio
---

{% include toc %}

# Introduction
- UAV as test platform for AUM project sensors
- Blimp uav with 4 rotors, 15m 5m radius
- crucial: hull pressure constant even if environment changes
  - active control system needed
- this system developed at FSD

# Methods
- MCU based system
- Two separate systems for redundancy
- Stacked fans as main actuators
  - this concept derived during previous work
- pressure sensors for differential pressure
- temperature sensors
  - digital for easy integration
- PID controller
- PCB for combining
- Comunication interface with CAN
- Firmware
  - OOP
  - software structure
  - super loop architecture

# Results
- System could regulate hull pressure
- Data broadcast via CAN
- debugging functions via serial 
  - e.g. tell temp sensors found but not integrated

# Conclusion 
- Hull pressure regulated, after PID tuning
- PCB experience 

# Outlook/Reflection
- should have used RTOS, though not time critical system/no hard deadlines
- system should have been on PCB directly not with breakout boards 
  - unnecessary weight and complexity. 
  - Even MCU could have been directly on the PCB
- 