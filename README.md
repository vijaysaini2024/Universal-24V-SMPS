# Universal AC-to-DC 24V SMPS - Schematic Architecture

## Overview
A comprehensive schematic design for a Switch Mode Power Supply (SMPS) engineered to convert universal AC mains input into a stable 24V DC output. 

Rather than rushing to a physical PCB layout, the primary focus of this project was to deeply analyze power electronics architecture and master advanced schematic capture techniques in KiCad. The goal was to ensure the design is readable, highly modular, and professionally documented for future layout routing.

## Hardware Architecture & Power Flow
* **Core Controller:** UC3844 Current-Mode PWM Controller.
* **AC Input & EMI Filter:** Includes transient protection (varistor) and an EMI choke.
* **HV Rectifier & DC Bus:** Full-bridge rectification to supply the high-voltage DC bus.
* **Switching & Isolation:** Drives an N-channel MOSFET (IRF840A) through a step-down transformer.
* **Feedback Loop:** Utilizes a PC817 optocoupler for safe, isolated voltage regulation across the isolation barrier.

## Schematic Organization & EDA Skills
A major focus was placed on transitioning from a standard net-wire design to a clean, industry-standard layout using KiCad's organizational features:
* Implemented **Local and Global Net Labels** to eliminate crossing wires and significantly improve readability.
* Grouped functional blocks (e.g., PWM Signal Control, Snubber Circuit, LV DC Output) using graphical bounding boxes.
* Structured the schematic to logically isolate the high-voltage mains sections from the low-voltage feedback logic.

## Visual Documentation

### Final Organized Architecture
![Final Schematic](Screenshot_2026-01-15_174832.png)

### Initial Draft & Routing Progression
![Initial Draft](Screenshot_2026-01-14_191114.png)

## Repository Contents
* **`/`** - Contains the native `.kicad_sch` and project files for direct examination.
