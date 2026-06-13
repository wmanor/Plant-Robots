\# Plant Watering Robot



\*\*Embedded systems project\*\* — Automatic plant watering system using a PIC24 microcontroller.



\## Overview

Built a soil moisture monitoring and automated watering device. The system continuously measures soil moisture using a resistive sensor and ADC, displays readings and status on an LCD screen, and activates a solenoid valve (via relay) when the soil is too dry.



Key features:

\- Real-time moisture percentage calculation with averaging filter

\- LCD output showing moisture % and status ("Too dry", "Normal", etc.)

\- Automated watering with timed solenoid control

\- Low-power relay latching for the valve



\## Technologies

\- \*\*Microcontroller\*\*: PIC24

\- \*\*Language\*\*: C (XC16 compiler)

\- \*\*Peripherals\*\*: ADC, I2C (for LCD), timers, GPIO/relays

\- \*\*Hardware\*\*: Soil moisture sensor (voltage divider), LCD display, solenoid valve + relay



\## How It Works

\- Samples analog voltage from moisture sensor → converts to percentage

\- Displays current moisture and plant status on LCD

\- Triggers watering (3 seconds) when moisture drops below threshold

\- Uses circular buffer for averaging noisy sensor readings



\## Repository Structure

\- `PlantRobots.X/` — MPLAB X project folder with source code

&#x20; - `Final\_Project.c` — Main program logic

&#x20; - `PlantRobot.c / PlantRobot.h` — Helper functions for buffering, LCD, and flow control

\- `readme\_plant\_robots.pdf` — Original project report



\## Setup Notes

This was developed for the PIC24FJ128GA010 or similar. Requires MPLAB X IDE and XC16 compiler to build.



\---



\*\*Project was completed as a part of my Computer Engineering degree in the course EE-2361 (Spring 2019).\*\*
