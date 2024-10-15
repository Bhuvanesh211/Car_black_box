# Black Box for Automobiles

## Introduction

The concept of the Black Box, commonly associated with airplanes, is critical for analyzing the root cause of accidents. However, its utility extends beyond just post-accident analysis. In the automotive industry, the Black Box can be used to proactively detect issues and monitor vehicle operations. Known as an Event Data Recorder (EDR) or Accident Data Recorder (ADR), this system can log important vehicle parameters, such as engine faults or overspeeding, allowing for proactive maintenance and better fleet management.

In today's fast-paced world, drivers may ignore safety regulations to meet tight schedules or make extra trips. By implementing a Black Box in automobiles, critical events can be recorded, enabling better monitoring and safety. The proposed solution will log important events, such as gear shifts, engine temperature, fuel consumption, and trip distance, for efficient vehicle management.

This system also provides a password-protected interface for authorized personnel to access logs or set the system time. Additionally, it can be extended as an IoT-based solution, exporting data to a cloud server for centralized monitoring.

## Requirement Details

### Default Screen:
- Displays current time, vehicle speed, and the latest event when in operation mode.

### Login Screen:
- Press UP or DOWN keys to access the password prompt.
- Password consists of 4 key presses, displayed as “*”.
- Wrong password retries are allowed (max 3 attempts every 15 minutes).
- Incomplete key press (3-second pause) returns to Default Screen.

### Main Menu:
- Contains two options: 
  - **View Log**
  - **Set Time**
- Navigate using UP/DOWN keys.
- Long press UP key to enter the selected menu.
- Long press DOWN key to log out.
- Inactivity for 5 seconds results in automatic logout.

### View Log:
- Displays all logged events, starting from index 0.
- Event format: `"EVENT NUMBER" "EVENT SIGNATURE" "EVENT TIME" "SPEED AT THE EVENT"`.
- Scroll through entries using UP/DOWN keys, with rollover at max log entries.
- Event capturing remains active even when viewing logs.
- Long press UP key to return to the main menu.

### Set Time:
- Displays the current time, with the seconds field blinking (field to be changed).
- Use UP key to increment time (rollover at max).
- Use DOWN key to select the next field.
- Long press UP key to return to the main menu.

### Event Capture:
- Captures and stores real-time events in memory.
- Event format: `"EVENT SIGNATURE" "EVENT TIME" "SPEED AT THE EVENT"`.
- Event logging continues regardless of the current system mode.

## System Features
- Proactive logging of critical events to detect potential issues.
- User-friendly interface with password protection.
- Extendible to a cloud-based IoT solution for centralized monitoring.

## Microcontroller used - PIC16F877A
## Developer Tools - MPLAB x IDE, MPLAB x XC8 (Compiler),PICSimlab
