---
lang: en
lang-niv: font
lang-ref: 021-jbk
layout: page
title: 'RasPY Utility'
---

# RasPY Utility

<div align="center">
  <img src="../images/logo.png" alt="RasPY Utility Logo" width="50%">
</div>

## Welcome to RasPY Utility Documentation

RasPY Utility is a comprehensive application for controlling and monitoring Raspberry Pi GPIO pins through an intuitive graphical interface or REST API.

## Table of Contents

### Introduction
- [Installation](installazione.md)
- [Guide](guida.md)

### Development
- [Development](sviluppo.md)
- [API](api.md)
- [GUI](gui.md)
- [Examples](esempi.md)

### Additional Resources
- [Changelog](changelog.md)
- [FAQ](faq.md)

### Community
- [Contribute](contribuire.md)
- [Acknowledgments](ringraziamenti.md)

## Key Features

### ✅ **Modern Graphical Interface**
- Dark/light theme
- Multi-language support
- Real-time pin status visualization
- System tray integration

### 🔌 **Complete GPIO Support**
- Digital I/O pin control
- Built-in simulator for development
- Automatic hardware detection
- Remote GPIO support

### 🌐 **Web Interface**
- Built-in web server
- Responsive design for mobile/desktop
- Real-time updates
- Integrated API documentation

## Quick Start

1. [Installation](installazione.md) - How to install and configure RasPY Utility
2. [Guide](guida.md) - Application usage guide
3. [API](api.md) - API documentation for developers
4. [Development](sviluppo.md) - Development and contribution guide

## User Guide

### Graphical Interface

The RasPY 4 Utility graphical interface is designed to be intuitive and easy to use.

#### Main Menu

- **File**: Application general controls
- **GPIO**: GPIO pin and simulator management
- **View**: Interface customization
- **Help**: Documentation and information

#### GPIO Control

1. Open the GPIO control window from the menu
2. Select the pin to control
3. Use the buttons to toggle pins
4. Monitor status in real-time

#### GPIO Simulator
The simulator allows you to test code without physical hardware:

1. Start the simulator from the GPIO menu
2. Use the interface to simulate input/output
3. Changes are reflected in real-time

### Logging and Debugging
The application logs important events in the `logs/app.log` file. Use the built-in Log Viewer to:

- Filter messages by level (INFO, WARNING, ERROR)
- Search for specific messages
- Export logs for analysis

### Keyboard Shortcuts

- **Ctrl+Q**: Quit the application
- **F1**: Show help
- **Ctrl+L**: Open log viewer
- **F5**: Refresh interface

## API Reference

### Overview

The RasPY 4 Utility REST API allows controlling GPIO pins via HTTP requests.
All responses are in JSON format.

### Available Endpoints

#### `GET /api/gpio`

Returns the status of all configured GPIO pins.

**Example response:**

```json
{
  "17": {"state": 0, "mode": "out", "description": "Red LED"},
  "18": {"state": 1, "mode": "in", "description": "Button"}
}
```

#### `GET /api/gpio/<int:pin>`

Returns the status of a specific pin.

**Parameters:**
- `pin`: GPIO pin number

**Status codes:**
- 200: Operation successful
- 404: Pin not found

**Example response:**

```json
{
  "state": 0,
  "mode": "out",
  "description": "Red LED"
}
```

#### `POST /api/gpio/<int:pin>/on`

Turns the specified pin on.

**Parameters:**
- `pin`: GPIO pin number

**Status codes:**
- 200: Operation successful
- 400: Invalid or non-writable pin

#### `POST /api/gpio/<int:pin>/off`

Turns the specified pin off.

**Parameters:**
- `pin`: GPIO pin number

**Status codes:**
- 200: Operation successful
- 400: Invalid or non-writable pin

## Usage Examples

### GPIO Control with Python

```python
import requests

BASE_URL = "http://localhost:5000/api/gpio"

# Get status of all pins
response = requests.get(f"{BASE_URL}")
print("Current status:", response.json())

# Turn on pin 17
response = requests.post(f"{BASE_URL}/17/on")
print("Turn on response:", response.status_code)
```

## Useful Resources

- [Official Raspberry Pi Website](https://www.raspberrypi.org/)
- [Python Documentation](https://www.python.org/)
