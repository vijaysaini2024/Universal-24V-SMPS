# Universal AC-to-DC 24V SMPS - Schematic Architecture

## Overview
A comprehensive schematic design for a Switch Mode Power Supply (SMPS) engineered to convert universal AC mains input into a stable 24V DC output. 

Rather than rushing to a PCB layout, the primary focus of this project was to deeply analyze power electronics architecture and master advanced schematic capture techniques in KiCad, ensuring the design is readable, modular, and professionally documented.

## Hardware Architecture & Power Flow
* **Core Controller:** UC3844 Current-Mode PWM Controller.
* **AC Input & EMI Filter:** Includes transient protection (varistor) and an EMI choke.
* **HV Rectifier & DC Bus:** Full-bridge rectification to supply the high-voltage DC bus.
* **Switching & Isolation:** Drives an N-channel MOSFET (IRF840A) through a step-down transformer.
* **Feedback Loop:** Utilizes a PC817 optocoupler for safe, isolated voltage regulation across the barrier.

## Schematic Organization & EDA Skills
A major focus was placed on transitioning from a standard net-wire design to a clean, industry-standard layout using KiCad's organizational features:
* Implemented **Local and Global Net Labels** to eliminate crossing wires and improve readability.
* Grouped functional blocks (e.g., PWM Signal Control, Snubber Circuit, LV DC Output) using graphical bounding boxes.
* Utilized hierarchical structuring principles to isolate the high-voltage sections from the low-voltage feedback logic.

## Visual Documentation

### Final Organized Architecture
*(Upload Screenshot 2026-01-15 174832.png to the repo and link it here)*
![Final Schematic](Screenshot_2026-01-15_174832.png)

### Initial Draft & Routing
*(Upload Screenshot 2026-01-14 191114.png to the repo and link it here)*
![Initial Draft](Screenshot_2026-01-14_191114.png)
