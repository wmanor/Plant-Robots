# Plant Watering Robot

Automatic house plant watering system using a PIC24 microcontroller.

## Overview
Built a soil moisture monitoring and automated watering device. The system continuously measures soil moisture using a resistive sensor and ADC, displays readings and status on an LCD screen, and activates a solenoid valve (via relay) when the soil is too dry.

### Key Features
- Real-time moisture percentage calculation with averaging filter
- LCD output showing moisture % and status ("Too dry", "Normal", etc.)
- Automated watering with timed solenoid control
- Low-power relay latching for the valve

## Technologies
- **Microcontroller**: PIC24 (XC16 compiler)
- **Language**: Embedded C
- **Peripherals**: ADC, I2C (LCD), Timers, GPIO/Relay
- **Hardware**: Resistive soil moisture sensor, LCD display, solenoid valve + relay

## How It Works
- Samples analog voltage from the moisture sensor and converts it to a percentage
- Uses a circular buffer for averaging noisy readings
- Displays current moisture level and plant status on the LCD
- Triggers watering cycle (3 seconds) when moisture falls below threshold

## Repository Structure
- `PlantRobots.X/` — MPLAB X project with all source code
  - `Final_Project.c` — Main program
  - `PlantRobot.c` / `PlantRobot.h` — Helper functions for sensor, LCD, and control logic
- `readme_plant_robots.pdf` — Original project report

---

Built as a part of the course EE-2361 in Spring 2019. 
Credit to Ames, who shopped for and assembled the hardware so I could spend the whole time coding. 
