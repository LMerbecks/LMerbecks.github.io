---
title: "Low-Cost Light Weight Robot Firmware"
excerpt: "Circular MIL-DTL-D38999 connectors are electrical connectors for rugged environments. Their design is scoop proof, contains polarization and separated electrical and mechanical connections. Due to high cost, use of these connectors in non-professional environments is low to non-existent. In this project a version of these connectors is developed that uses additive manufacturing and commonly available stamped electrical contacts to achieve a cost below 1€ for the smallest connector system.<br/><img src='/images/D389993MF/38999_cover.jpeg'>"
collection: portfolio
---

{% include toc %}

# Introduction
- goal: robot with learn and repeat function, serial interface. 
- start: 
  - robot hardware mostly finished
  - rudimental firmware

# Methods 
- servo control library
  - improved previous work made more clear
- Unblocking
  - previous firmware used blocked features
- Architecture
  - State machine
  - Serial interface/protocoll
- Documentation
  - Documentation with doxygen and sphinx
- Teensy 4.1 MCU, debug board (RS485 bridge)

# Results
- Functions: 
  - State machine representation from documentation
- Comprehensive documentation
- Unblocking
- MATLAB visualization and inverse kinematics

# Conclusion
- Robot with follow me function
- MATLAB interface
- joint protection
- emergency stop

# Outlook
- should have been ROS (would that have worked on the Teensy? I think not!)
- RTOS system (FreeRTOS e.g., would have been easy to implement tasks)
- Streamline USB protocol, too much data, binary would have been more efficient
- ROS like firmware implementation (nodes, topics, subscription etc.)...
