# ESP32 IoT Temperature Monitoring System
## Installation and Configuration Guide

### Document Information

| Field | Details |
|---|---|
| Document Type | Installation and Configuration Guide |
| Version | 1.1 |
| Author | Aditi S. Puranik |
| Audience | Beginner users, students, and support teams |
| Estimated Reading Time | 8 minutes |

---

## Purpose

This guide explains how to install and configure an ESP32-based temperature monitoring system using a DHT11 or DHT22 sensor. The system reads temperature and humidity values and displays the output through the Arduino IDE Serial Monitor or an IoT dashboard.

## Audience

This guide is intended for:

- Students working on beginner IoT projects
- Users setting up ESP32-based sensor systems
- Support teams troubleshooting basic IoT device setup issues

## Prerequisites

Before starting, make sure you have:

- Basic knowledge of electronics connections
- Arduino IDE installed on your laptop
- ESP32 board package installed in Arduino IDE
- A working USB cable
- Stable power supply
- Basic understanding of sensors and microcontroller boards

## Components Required

| Component | Quantity | Purpose |
|---|---:|---|
| ESP32 development board | 1 | Main microcontroller |
| DHT11 or DHT22 sensor | 1 | Measures temperature and humidity |
| Jumper wires | 3–4 | Connects sensor to ESP32 |
| Breadboard | 1 | Supports circuit connection |
| USB cable | 1 | Connects ESP32 to laptop |

## System Overview

The temperature sensor collects environmental data and sends it to the ESP32 board through a data pin. The ESP32 processes the sensor values and displays them through the Serial Monitor or sends them to a connected IoT dashboard.

**Basic flow:**

`DHT Sensor → ESP32 Board → Serial Monitor / IoT Dashboard`

## Wiring Details

| Sensor Pin | ESP32 Pin | Description |
|---|---|---|
| VCC | 3.3V | Provides power to the sensor |
| GND | GND | Completes the circuit |
| Data | GPIO 4 | Sends sensor data to ESP32 |

### Pinout Note

Common ESP32 development boards may have slightly different physical labeling or layouts, even though the GPIO numbers remain the same. Always verify the board pin labels before making connections.

For example:

- GPIO 4 may be labeled as IO4 on some boards.
- The position of 3.3V and GND pins can vary depending on the ESP32 board version.
- Some boards include multiple GND pins, and any valid GND pin can usually be used.

If you are using a different ESP32 board model, check the board's pinout diagram before wiring the sensor.

## Wiring Diagram

**Figure 1:** Basic connection between DHT sensor and ESP32 board.

*Wiring diagram to be added.*

**Connection summary:**

- DHT VCC → ESP32 3.3V
- DHT GND → ESP32 GND
- DHT Data → ESP32 GPIO 4

## Quick Start

1. Connect the DHT sensor to the ESP32 board.
2. Open Arduino IDE.
3. Select the correct ESP32 board and COM port.
4. Install the required DHT sensor library.
5. Upload the code to the ESP32 board.
6. Open Serial Monitor.
7. Verify the temperature and humidity readings.

## Verification

If the setup is correct, the Serial Monitor should display output similar to:

```text
Temperature: 28.6°C
Humidity: 62%
```

If the values appear at regular intervals, the device is working correctly.

## Troubleshooting

| Issue | Possible Cause | Recommended Action |
|---|---|---|
| ESP32 not detected | USB cable or driver issue | Try another USB cable and check the COM port |
| No sensor reading | Loose wiring | Recheck VCC, GND, and data pin connections |
| Upload failed | Wrong board selected | Select the correct ESP32 board in Arduino IDE |
| Incorrect readings | Sensor placed near heat source | Move the sensor to a normal room-temperature area |
| Output shows NaN | Sensor data not received | Check the data pin and sensor library |

## Safety Notes

- Do not connect the sensor to a voltage higher than the recommended limit.
- Disconnect the USB cable before changing connections.
- Avoid loose wires while testing the circuit.
- Keep the sensor away from direct heat sources during testing.

## FAQ

### Why is my ESP32 not showing in Arduino IDE?

This may happen due to a faulty USB cable, missing driver, or incorrect COM port selection. Try reconnecting the board and selecting the correct port.

### Can I use DHT22 instead of DHT11?

Yes. DHT22 can be used instead of DHT11. However, the code and library settings should match the selected sensor.

### Why am I getting incorrect temperature values?

Incorrect values may occur due to loose wiring, incorrect sensor type selection, or sensor placement near a heat source.

## Glossary

| Term | Meaning |
|---|---|
| ESP32 | A microcontroller board commonly used in IoT projects |
| GPIO | General Purpose Input/Output pin used to connect components |
| Sensor | A device that detects physical conditions such as temperature |
| Serial Monitor | A tool in Arduino IDE used to view output from the board |
| IoT | Internet of Things, a system of connected devices that collect and share data |

## Revision History

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | Initial documentation sample created |
| 1.1 | June 2026 | Added pinout note, wiring diagram section, and improved verification formatting |
