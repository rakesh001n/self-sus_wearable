# KinetiWatch: Motion-Powered Smart Wearable

## Overview

KinetiWatch is an innovative smart wearable watch that harnesses the natural movements of the human body to generate sustainable power through three complementary energy harvesting technologies:

- **Piezoelectric harvesting**: Converts mechanical stress from movement into electrical energy
- **Triboelectric harvesting**: Generates electricity from friction between materials during motion
- **Thermoelectric harvesting**: Utilizes the temperature difference between the human body and the ambient environment

This project aims to create a sustainable, eco-friendly smart watch that drastically reduces the need for traditional battery charging while providing full smart watch functionality.

## Features

- **Multi-source energy harvesting**
  - Piezoelectric generation from wrist flexion and arm movement
  - Triboelectric generation from sliding and contact-separation modes
  - Thermoelectric generation from body-ambient temperature differential

- **Power Management**
  - Intelligent power routing from multiple energy sources
  - Ultra-low-power microcontroller for system control
  - Power storage optimization for extended usage

- **User Experience**
  - Standard smart watch functionality (time, notifications, activity tracking)
  - Energy generation feedback display
  - Battery status monitoring with power conservation modes

## Technical Architecture

### Hardware Components

- Custom PCB with integrated energy harvesting circuits
- Energy storage system (supercapacitors and LiPo battery hybrid)
- Low-power display (E-ink or OLED with selective refresh)
- ARM Cortex-M4F microcontroller (STM32L4 series)
- Bluetooth Low Energy module for connectivity
- Sensors: accelerometer, heart rate, temperature

### Energy Harvesting Systems

- **Piezoelectric Module**
  - PZT ceramic transducers strategically placed at high-stress points
  - Frequency-tuned cantilever beams for optimal energy capture
  - AC-DC converter with impedance matching circuit

- **Triboelectric Module**
  - PTFE and nylon contact surfaces in sliding configuration
  - Copper electrodes with low-impedance connections
  - Specialized rectifier circuit for high-voltage, low-current output

- **Thermoelectric Module**
  - Bismuth Telluride (Bi₂Te₃) thermopiles
  - Optimized heat sink design for ambient side
  - DC-DC boost converter for voltage regulation

### Power Management

- Intelligent power routing system for prioritizing energy sources
- Deep sleep modes with context-aware wake-up triggers
- Adaptive functionality based on available power

## Getting Started

### Prerequisites

- Arduino IDE or STM32CubeIDE
- PCB fabrication capabilities or access to PCB manufacturing services
- 3D printer for case prototyping
- Electronic testing equipment (oscilloscope, multimeter, power analyzer)

### Build Instructions

1. Clone this repository
   ```
   git clone https://github.com/yourusername/kinetiwatch.git
   ```

2. Review the `/hardware` directory for PCB designs and component list

3. Fabricate the PCB or use the provided Gerber files with a PCB manufacturing service

4. Assemble the hardware components following the documentation in `/docs/assembly.md`

5. Flash the firmware using the instructions in `/firmware/README.md`

6. 3D print the case using the provided STL files in `/hardware/case/`

7. Assemble the final product using the guidelines in `/docs/final_assembly.md`

## Project Structure

```
kinetiwatch/
├── firmware/                 # Source code for the device firmware
│   ├── main/                 # Main application code
│   ├── drivers/              # Hardware interface drivers
│   └── power_management/     # Energy harvesting and power management
├── hardware/                 # Hardware design files
│   ├── schematics/           # Electrical schematics
│   ├── pcb/                  # PCB layout files
│   └── case/                 # 3D models for the watch case
├── docs/                     # Documentation
│   ├── theory/               # Energy harvesting theory
│   ├── testing/              # Test procedures and results
│   └── assembly/             # Assembly instructions
└── tools/                    # Support tools and utilities
```

## Current Status

This project is currently in the prototype phase. We have successfully:

- Developed and tested individual energy harvesting modules
- Created an integrated power management system
- Implemented basic firmware functionality
- Designed an ergonomic case prototype

We are actively working on:

- Optimizing the power conversion efficiency
- Reducing the overall form factor
- Extending the functionality of the companion app
- Improving the user interface

