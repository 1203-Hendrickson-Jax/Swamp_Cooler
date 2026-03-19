# Embedded Swamp Cooler Control System

## Overview
This project is an embedded systems implementation of an automated swamp cooler controller built on Arduino-compatible hardware. It monitors environmental conditions, controls a fan and vent system, detects low water levels, and provides user feedback through an LCD, status LEDs, a real-time clock, and serial output.

The system was designed to simulate a real-world cooling controller that can automatically respond to temperature, humidity, and water availability while allowing manual user interaction.

---

## Features
- Monitors **temperature and humidity** using a DHT11 sensor
- Detects **water level status** and enters an error state when water is too low
- Automatically activates cooling when environmental thresholds are exceeded
- Controls a **motor-driven cooling system**
- Rotates vents using a **stepper motor**
- Displays live system information on an **LCD screen**
- Tracks and prints timestamps using a **real-time clock (RTC)**
- Uses **status LEDs** to indicate:
  - Disabled
  - Idle
  - Running
  - Error
- Outputs system messages, temperature, humidity, and timestamps through **serial communication**
- Supports **manual on/off control** and user vent adjustment

---

## Hardware / Components
- Arduino-compatible microcontroller
- DHT11 temperature/humidity sensor
- RTC module (DS1307)
- LCD display
- Stepper motor
- Water level sensor
- DC motor / fan control
- Status LEDs
- Push buttons / interrupts

---

## Technologies Used
- C++
- Arduino framework
- Embedded systems programming
- Sensor integration
- Serial communication
- Register-level UART and ADC interaction
- Real-time hardware control

---

## Key Concepts Demonstrated
- Embedded state-machine style control logic
- Sensor-driven automation
- Hardware/software integration
- Stepper motor and fan control
- Real-time monitoring and user feedback
- Register-level programming for UART and ADC
- Fault detection and safe-state transitions

---

## System Behavior
The controller operates in several system states:

- **Disabled:** system is off
- **Idle:** system is on, but temperature/humidity are below activation thresholds
- **Running:** fan and cooling system are active
- **Error:** water level is too low for safe operation

When temperature or humidity exceed defined thresholds, the system activates cooling automatically. If the water sensor detects a low water level, the system halts cooling and enters an error state until the issue is resolved.

---

## Inputs and Outputs

### Inputs
- Temperature and humidity readings
- Water level sensor
- On/off buttons
- Vent rotation buttons

### Outputs
- LCD display status updates
- LED state indicators
- Fan motor control
- Stepper motor vent control
- Serial monitor logs with timestamps

---

## Notable Implementation Details
- Uses a **real-time clock** to log system events with timestamps
- Includes **register-level UART and ADC functions** rather than relying only on high-level abstractions
- Supports both **automatic cooling behavior** and **manual vent adjustment**
- Prints periodic environmental readings for runtime monitoring

---

## What I Learned
- How to design and implement an embedded control system
- How to integrate multiple hardware devices into a single coordinated project
- How to manage system states and transitions safely
- How to combine low-level register manipulation with higher-level hardware libraries
- How real-world constraints like sensor thresholds and fault handling affect embedded design

---

## Future Improvements
- Replace blocking delays with timer-based scheduling
- Improve modularity by separating logic into state-specific functions
- Add more robust debounce handling for button input
- Use non-blocking event-driven control for smoother system response
- Add more precise calibration for sensor thresholds
- Expand logging and diagnostics for debugging

---

## Summary
This project demonstrates embedded systems design through the development of a sensor-driven cooling controller that integrates automation, hardware control, fault detection, and user interaction into a single real-time system.
