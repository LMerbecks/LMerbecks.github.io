---
title: "Blimp UAV Propulsion System Tilt Actuator Software"
excerpt: "Circular MIL-DTL-D38999 connectors are electrical connectors for rugged environments. Their design is scoop proof, contains polarization and separated electrical and mechanical connections. Due to high cost, use of these connectors in non-professional environments is low to non-existent. In this project a version of these connectors is developed that uses additive manufacturing and commonly available stamped electrical contacts to achieve a cost below 1€ for the smallest connector system.<br/><img src='/images/D389993MF/38999_cover.jpeg'>"
collection: portfolio
---

{% include toc %}

# Introduction
- UAV for AUM sensor test platform
- blimp with 15m x 5m length
- 4 propellers for thrust and control (3d thrust vectoring every actuator 1D)
- system and firmware needed for implementation
- translate CAN signals to RS485

# Methods
- automotive part (can gateway)
- using custom firmware
- software architecture
  - calibration functions
    - because position was lost after power down
- implementations?


# Results
- could move as expected
- calibration worked
- system flew on UAV
- problems?

# Conclusion
- system firmware with C
- OOP-ish
- main functions + additional

# Outlook/Reflection
- Direct electronic implementation of CAN to RS485 translator
  - MCU and transceivers on PCB
  - not done due to lack of experience 
- calibration feature should have used both end stops
  - thus no need for hard coded offset
- offsets changeable by CAN