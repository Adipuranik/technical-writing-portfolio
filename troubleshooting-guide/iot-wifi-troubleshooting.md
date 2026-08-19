# IoT Wi-Fi Connectivity Issues
## Troubleshooting Guide

### Document Information

| Field | Details |
|---|---|
| Document Type | Knowledge Base Article |
| Version | 1.0 |
| Author | Aditi S. Puranik |
| Audience | IoT users, students, and support teams |
| Estimated Reading Time | 6 minutes |

---

## Issue Summary

This article explains how to troubleshoot common Wi-Fi connectivity issues in IoT devices, such as ESP32-based sensors, smart monitoring systems, and other wireless embedded devices.

## Affected Devices

This guide applies to:

- ESP32-based IoT devices
- Wi-Fi-enabled sensor systems
- Smart monitoring devices
- IoT dashboards connected through cloud platforms

## Common Symptoms

Users may experience one or more of the following:

- Device does not connect to Wi-Fi
- Device connects but disconnects frequently
- Data does not update on the dashboard
- Device works on a mobile hotspot but not on home Wi-Fi
- Device status shows offline

## Likely Causes

| Cause | What It Means |
|---|---|
| Incorrect Wi-Fi credentials | The Wi-Fi name (SSID) or password is entered incorrectly |
| Weak signal strength | The device is too far from the router or there is interference |
| Unsupported Wi-Fi band | The network is 5 GHz only; many IoT devices require 2.4 GHz |
| Power supply issue | Unstable power causes resets or intermittent disconnects |
| Cloud/API configuration error | The dashboard token, API key, or endpoint is incorrect |

## Step-by-Step Resolution

Follow these steps in order. After each step, reconnect the device and check whether it remains online.

### Step 1: Confirm the Wi-Fi Name and Password

Re-enter the Wi-Fi name and password carefully. Check spelling, capitalization, and special characters.

### Step 2: Confirm the Wi-Fi Band

Many IoT devices support only **2.4 GHz Wi-Fi**.

If your router is using only 5 GHz, connect the device to a 2.4 GHz network.

Some routers use the same network name (SSID) for both 2.4 GHz and 5 GHz. In this situation, you may need to separate the SSIDs or temporarily disable 5 GHz during setup.

### Step 3: Improve Signal Strength

Place the IoT device closer to the router during setup to reduce connection drops.

### Step 4: Restart the Router and Device

Turn off the router and IoT device, wait approximately **30 seconds**, and then turn them back on.

### Step 5: Verify Dashboard or Cloud Settings

If the device is connected to Wi-Fi but data is not updating, verify:

- Dashboard token
- API key
- Cloud configuration
- Endpoint configuration

## Troubleshooting Reference

| Problem | Most Likely Cause | Recommended Action |
|---|---|---|
| Device not connecting | Incorrect Wi-Fi credentials | Re-enter the SSID and password |
| Device disconnects frequently | Weak Wi-Fi signal | Move the device closer to the router and retry |
| Dashboard not updating | Cloud/API configuration error | Confirm the API key/token and dashboard settings |
| Works on hotspot but not router | Unsupported Wi-Fi band | Connect to a 2.4 GHz network |
| Device shows offline intermittently | Power supply issue | Use a stable power source and recheck connections |

## Escalation

Escalate the issue if:

- The device does not connect after verifying credentials and Wi-Fi band.
- The device restarts repeatedly.
- Firmware upload fails multiple times.
- The dashboard does not receive data after confirming the configuration.

### Information to Collect Before Escalation

Record the following information:

- Device model
- Wi-Fi network type (2.4 GHz or 5 GHz)
- Error messages from the Serial Monitor, logs, or dashboard
- Screenshot of the dashboard
- Troubleshooting steps already attempted

## Prevention Tips

- Use a stable 2.4 GHz Wi-Fi network for IoT setup.
- Keep the device within a reliable signal range.
- Use a stable power source.
- Store Wi-Fi credentials and dashboard tokens securely.
- Test with a mobile hotspot to isolate router or network issues.

## FAQ

### Why does my IoT device connect to a hotspot but not my router?

This may occur if the router uses a 5 GHz network or has security settings that prevent the device from connecting. Try using a 2.4 GHz network and review the router settings.

### Why is my dashboard not showing live data?

The device may be connected to Wi-Fi but not sending data to the dashboard. Check the API key or token, cloud configuration, and sensor readings.

### Why does my device keep disconnecting?

Frequent disconnections may be caused by a weak Wi-Fi signal, unstable power supply, or firmware issues.

## Glossary

| Term | Meaning |
|---|---|
| Wi-Fi Band | Frequency used by a Wi-Fi network, typically 2.4 GHz or 5 GHz |
| API Key | A code used to authenticate a device or application with a service |
| Dashboard | An interface that displays device data |
| Firmware | Software installed on a hardware device |
| Router | A device that provides network and internet connectivity |

## Revision History

| Version | Date | Change |
|---|---|---|
| 1.0 | June 2026 | Initial knowledge base article created |
