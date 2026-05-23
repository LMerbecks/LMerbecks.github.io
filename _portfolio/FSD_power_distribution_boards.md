---
title: "Blimp UAV Power Distribution Boards"
excerpt: "Circular MIL-DTL-D38999 connectors are electrical connectors for rugged environments. Their design is scoop proof, contains polarization and separated electrical and mechanical connections. Due to high cost, use of these connectors in non-professional environments is low to non-existent. In this project a version of these connectors is developed that uses additive manufacturing and commonly available stamped electrical contacts to achieve a cost below 1€ for the smallest connector system.<br/><img src='/images/D389993MF/38999_cover.jpeg'>"
collection: portfolio
---

{% include toc %}

# Introduction 
- UAV for AUM at FSD as testplatform
- blimp with 15m x 5m dimensions
- multiple voltage levels in different systems
- centralized power distribution wanted
- implementation described here

# Methods
- ideal diodes for power combination
- external DCDC converters
- connectors molex 
  - pin assignment
- PCBs for integration
  - using KiCad
  - simple schematics
- Also relay boards for external power delivery
- emergency board (?)
- SMT and THT combination

# Results
- combination worked
- manufacturable
- compatible with mechanical constraints
- stackable
- sufficient current capacity

# Conclusion
- Power distribution streamlined
- redundancy integrated into PCB
- PCB experience enhanced

# Outlook/Review
- Thermal simulations (joule heating)
- DCDC Converter on board
- 