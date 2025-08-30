---
lang: zh
lang-niv: font
lang-ref: 012-jbk
layout: page
title: 'CDE550-Sim'
---

# Nidec Commander CDE 550 Simulator

[![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Version](https://img.shields.io/badge/version-0.0.2-green.svg)](CHANGELOG.md)

Software simulator for the Nidec Commander CDE 550 inverter with a graphical interface, developed in Python with PyQt6.

## What's New in Version 0.0.2

- **Complete localization** of the user interface in Italian
- **Improved alarm handling** with reduced false positives
- **Performance optimizations** during startup and load variations
- **Updated documentation** with detailed CHANGELOG

## Features

- Realistic simulation of Nidec Commander CDE 550 inverter behavior
- Intuitive graphical interface with PyQt6 fully localized in Italian
- Serial communication via pyserial
- Support for main control commands
- Fault and alarm simulation with advanced management
- Real-time parameter monitoring
- Event and error logging

## Prerequisites

- Python 3.8 or higher
- Pip (Python package manager)
- Python virtual environment (recommended)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Nsfr750/CDE550-sim.git
   cd CDE550-sim
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   # On Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # On macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the simulator:
   ```bash
   python main.py
   ```

2. The graphical interface will show:
   - Inverter status
   - Operating parameters
   - Event log
   - Simulation controls

3. For serial connection:
   - Go to Connection -> Connect
   - Select the desired COM port
   - Set the communication speed (baud rate)
   - Click "Connect"

## Supported Serial Commands

| Command | Description | Example |
|---------|-------------|---------|
| `RUN` | Start the inverter | `RUN` |
| `STOP` | Stop the inverter | `STOP` |
| `RST` | Reset alarms | `RST` |
| `FREQ <value>` | Set frequency (Hz) | `FREQ 50.0` |
| `DIR <1\|-1>` | Set direction | `DIR 1` (forward) |
| `STATUS` | Show complete status | `STATUS` |
| `HELP` | Show command list | `HELP` |

## Project Structure

```
CDE550-sim/
├── main.py              # Application entry point
├── inverter_sim.py      # Inverter simulation logic
├── serial_handler.py    # Serial communication handling
├── script/              # User interface and help files
│   ├── help.py          # Help window
│   ├── serial_dialog.py # Serial connection window
│   └── version.py       # Version management
├── requirements.txt     # Project dependencies
├── README.md            # Main documentation
└── CHANGELOG.md         # Change log
```

## Contributing

Contributions are welcome! To propose improvements:

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the GPL-3.0 License. See `LICENSE` for more information.

## Contact

- Author: Nsfr750
- Email: [nsfr750@yandex.com]
- Repository: https://github.com/Nsfr750/CDE550-sim

