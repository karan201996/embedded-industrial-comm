# Embedded Industrial Communication  
## Overview  
This project adds industrial communication capabilities to a microcontroller by implementing Modbus (RTU/ASCII) and CAN bus protocols. It demonstrates how to develop protocol stacks, handle message framing/parsing, and integrate the MCU with industrial equipment.  
## Hardware Requirements  
- STM32 MCU with CAN peripheral (e.g., STM32F103 or STM32G4 series).    
- RS‑485 transceiver for Modbus RTU communication.    
- CAN transceiver (e.g., MCP2562).    
- Optional: industrial sensors or actuators for demonstration.    
## Software Requirements  
- STM32 HAL or Low‑Layer drivers.    
- Modbus library (e.g., FreeModbus) or custom implementation.    
- CAN driver support.    
- CMake build system or STM32CubeIDE.    
## Build & Flash Instructions  
1. Clone this repository and configure the project for your target MCU.    
2. Enable and configure UART/RS‑485 and CAN peripherals in the code.    
3. Build the firmware with CMake (`cmake . && make`) or using STM32CubeIDE.    
4. Flash the binary using ST‑Link.    
5. Connect the MCU to a Modbus master or CAN network for testing.    
## Features  
- Modbus RTU/ASCII slave implementation with configurable registers and coils.    
- CAN bus driver supporting standard and extended frames.    
- Example application reading sensor values and exposing them via Modbus and CAN.    
- Basic error handling and bus timeout detection.    
## Demo  
Use a Modbus master tool (such as Modscan) to read the MCU’s holding registers over RS‑485. For CAN, connect a CAN analyser and observe the transmitted frames containing sensor data.    
## Future Work  
- Add Modbus TCP support over Ethernet.    
- Implement a gateway between Modbus and CAN networks.    
- Integrate real industrial sensors and actuators for a more complete demo. 
