# STR_PCB

Custom PCB design for the low-level controller of the STR Robot autonomous vehicle platform.

## Overview

This repository contains the hardware design files for the custom controller board used in the STR Robot project. The board is designed to interface with the STM32-based firmware layer and provide the electrical bridge between the vehicle hardware and the ROS 2 autonomy stack.

This repository is part of the complete STR Robot simulation-to-reality system:
- custom PCB hardware
- STM32 micro-ROS firmware
- ROS 2 autonomy workspace
- real-world Ackermann robot deployment

## Board Preview


<img width="669" height="723" alt="image" src="https://github.com/user-attachments/assets/ee5d8abd-49ce-4d4a-af29-ec5567cc5124" />


## Schematic Preview

<img width="1265" height="861" alt="image" src="https://github.com/user-attachments/assets/1746ea42-81f0-4d3d-9dd1-b80717482706" />


**Schematic PDF:** [schematicf4.pdf](https://github.com/user-attachments/files/26848001/schematicf4.pdf)

## Repository Contents

- `f4_v2.kicad_sch` — KiCad schematic
- `f4_v2.kicad_pcb` — KiCad PCB layout
- `f4_v2.kicad_pro` — KiCad project file
- `Gerber_f4_v2/` — exported Gerber manufacturing files
- `Gerber_f4_v2.zip` — compressed Gerber package
- `f4_v2-backups/` — backup files

## Purpose

The board is designed as the low-level control hardware for the STR Robot platform. It supports the embedded controller responsible for:
- motor-related interfaces
- steering-related interfaces
- encoder and GPIO connections
- serial communication interfaces
- integration with the STM32 micro-ROS firmware layer

## System Role

This repository corresponds to the **hardware layer** of the full robot system:

`STR_PCB` → `microros_ws` → `ttbot_ws`

- **STR_PCB**: custom controller board
- **microros_ws**: STM32-based embedded firmware using micro-ROS
- **ttbot_ws**: high-level ROS 2 workspace for localization, planning, and navigation

## Hardware Interfaces

From the current board design, the PCB provides grouped connectors for:
- **GPIO**
- **ENCODER**
- **MOTOR**
- **UART / serial communication**
- power input / output terminals

## Toolchain

- KiCad for schematic and PCB design
- Standard Gerber export for PCB fabrication

## Manufacturing

To fabricate the board:
1. Open the project in KiCad
2. Review the schematic and PCB layout
3. Export or use the provided Gerber files in `Gerber_f4_v2/`
4. Submit the Gerber package to your PCB manufacturer

## Related Repositories

- Firmware: [`microros_ws`](https://github.com/Nvinh5148/microros_ws)
- ROS 2 autonomy stack: [`ttbot_ws`](https://github.com/Uyle-gif/ttbot_ws)

## Project Context

This board is part of the STR Robot simulation-to-reality development pipeline for an Ackermann-steered autonomous mobile robot.
