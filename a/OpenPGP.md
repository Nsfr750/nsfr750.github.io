---
lang: en
lang-niv: fonto
lang-ref: 018-jbk
layout: page
title: 'OpenPGP'
---


# OpenPGP GUI App Documentation

Welcome to the official documentation for the **OpenPGP GUI App**.

## Overview
This application provides a modern, user-friendly interface for OpenPGP key management, encryption, decryption, message signing, verification, and SSL certificate generation. All cryptographic operations are performed locally for maximum privacy.

# Features

- Modern UI with ttkbootstrap (Superhero theme)
- Generate, load, and export OpenPGP key pairs
- Set key name, email, passphrase, and view fingerprint
- Encrypt and decrypt messages
- Sign and verify messages (detached signatures)
- Export public key in ASCII-armored format (.asc)
- Visualize key fingerprint for security checks
- Generate SSL certificates with custom CN
- Clear/reset all fields with one click
- **Centralized logging system** (info, warning, error, uncaught exceptions)
- **Log Viewer with real-time filtering** (ALL, INFO, WARNING, ERROR)
- Use `log_info`, `log_warning`, `log_error` for custom log entries
- Automatic traceback capture and display in log viewer
- Dynamic menu bar with About, Help, Log Viewer, Sponsor, Version dialogs
- Semantic versioning and version info
- Modular structure (`struttura`, `gui`, etc.)
- Easy extensibility and theming (via ttkbootstrap)

# Getting Started

## Requirements
- Python 3.9 or higher
- PySide6 (included in requirements)
- pgpy (included in requirements)
- cryptography (included in requirements)
- pyperclip (included in requirements)

> **Note**: The application has been migrated from Tkinter/ttkbootstrap to PySide6 for a more modern and maintainable UI.

## Installation
1. Clone or download this repository.
2. (Optional) Create a virtual environment:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Running the App
Run from the project root:
```
python main.py
```

If you see import errors, ensure you are running from the root and not inside a subfolder.

# User Guide

## Main Window Overview
- Enter your name, email, and passphrase for key generation.
- Select the algorithm (currently RSA; more coming soon).
- Use the buttons to generate, load, or export keys.
- The fingerprint of the loaded/generated key is shown for verification.
- Use the text area to input messages for encryption, decryption, signing, or verification.
- Export your public key to share it securely.
- Generate SSL certificates from the GUI.
- Use the 'Clear' button to reset all fields.

## Menu Bar
- **File**: Export public key, Exit
- **Log**: View log (with filters for ALL, INFO, WARNING, ERROR)
- **Help**: Help, About, Sponsor

## Logging & Log Viewer
- All info, warnings, errors, and uncaught exceptions are logged automatically.
- Use `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` in your scripts for custom logging.
- The Log Viewer (Log > View Log) allows you to filter and view logs by level.
- If the log file is missing, the last runtime traceback is shown if available.

## Tips
- All cryptographic operations are local (no cloud).
- For best results, use strong passphrases.
- The log window provides feedback and error details.

# Advanced Usage

## Exporting Public Keys
- Use the 'Export Public Key' button or menu item to save your public key in ASCII-armored format (.asc).

## Fingerprint Verification
- Always check the fingerprint before sharing your public key for added security.

## SSL Certificate Generation
- Enter the desired Common Name (CN) in the name field.
- Click the 'Generate SSL Certificate' button to create a self-signed certificate.

## Extending the App
- You can add support for more algorithms (ECC, Ed25519) by extending the key generation logic in `main_window.py`.
- The GUI uses ttkbootstrap for easy theming and customization.

## Logging & Debugging
- All actions, warnings, errors, and uncaught exceptions are logged to `traceback.log`.
- Use `log_info`, `log_warning`, `log_error` for custom log entries in your code.
- The Log Viewer supports filtering by ALL, INFO, WARNING, ERROR.
- If the log file is missing, the last runtime traceback is displayed.

## Troubleshooting
- If you encounter import errors, ensure you are running from the project root.
- For issues with dependencies, check `requirements.txt` or reinstall the needed packages.

# Developer Guide

Welcome, developer! This guide provides the essentials for contributing to and extending the OpenPGP GUI App.

---

## Project Structure
- `main.py` — Entry point, launches the main window.
- `gui/` — All GUI components (main window, widgets, dialogs).
- `struttura/` — Core logic, dialogs, utilities, versioning, help/about, etc.
- `docs/` — Documentation.
- `requirements.txt` — Python dependencies.

## Key Technologies
- **Python 3.x**
- **Tkinter** — GUI framework (with ttkbootstrap for theming)
- **pgpy** — OpenPGP cryptography
- **cryptography** — SSL certificate generation
- **Pillow** — (optional) for icons

## How to Contribute
1. Fork and clone the repository.
2. Create a virtual environment and install dependencies.
3. Follow PEP8 and keep code modular.
4. Document new features and update `CHANGELOG.md`.
5. Add or update tests if possible.
6. Open a pull request with a clear description.

## Adding Features
- To add new algorithms (e.g., ECC), extend the key generation logic in `main_window.py`.
- For new GUI components, add widgets in `gui/` and keep logic separate from UI.
- Use `ttkbootstrap` styles for a consistent look.

## Testing
- Add tests for new features and bugfixes.
- Manual testing: run `python main.py` and use all GUI functions.
- (Optional) Integrate with CI/CD for automated tests.

## Code Style
- Follow PEP8.
- Use docstrings for public functions/classes.
- Keep UI and logic as separate as possible.

## Logging & Debugging
- Use `log_info(msg)`, `log_warning(msg)`, `log_error(msg)` anywhere in the code for custom log entries.
- All logs are saved in `traceback.log` and shown in the Log Viewer.
- The Log Viewer supports filtering by ALL, INFO, WARNING, ERROR.
- Uncaught exceptions are automatically logged and shown in the Log Viewer (with traceback).

## Support & Questions
- Open issues on GitHub for bugs or feature requests.
- See `README.md` for contact and contribution info.

---

## Advanced Topics

### API Reference

The application is modular: core logic is in `struttura/`, GUI in `gui/`.

**Main classes and functions:**
- `MainWindow` (`gui/main_window.py`): Main GUI logic and event handling.
- `gen_key`, `export_pubkey`, `clear_fields`, etc.: Methods for cryptographic operations.
- `Help`, `About`, `LogViewer`, etc.: Dialogs and utilities in `struttura/`.
- `get_version()` (`struttura/version.py`): Returns current version string.

For more, read the docstrings in the code and see `docs/user_guide.md` for usage flow.

### Extension Examples

#### Adding a New Key Algorithm
1. In `gui/main_window.py`, locate the algorithm selection dropdown.
2. Add your new algorithm (e.g., ECC, Ed25519) to the dropdown options.
3. In the key generation logic, implement the handling for the new algorithm using `pgpy`.
4. Test thoroughly and update the documentation.

#### Adding a Custom Widget
1. Create your widget in `gui/widgets.py` or a new file.
2. Import and use it in `main_window.py` where needed.
3. Follow ttkbootstrap style conventions for consistency.

### Architectural Diagram

Below is a simple textual architecture overview:

```
OpenPGP GUI App
│
├── main.py (entry point)
│
├── gui/
│   ├── main_window.py (MainWindow class, event logic)
│   ├── widgets.py (custom widgets)
│   └── ...
│
├── struttura/
│   ├── help.py, about.py, version.py (dialogs, versioning)
│   ├── menu.py (menu bar logic)
│   └── ...
│
├── docs/ (documentation)
├── requirements.txt
└── ...
```

For a visual diagram, see [docs/architecture.png](architecture.png) (add your own PNG for more detail).

# FAQ

**Q: Can I use this app without an internet connection?**  
A: Yes! All cryptographic operations are performed locally for privacy.

**Q: How do I export my public key?**  
A: Use the 'Export Public Key' button or menu item in the File menu.

**Q: What algorithms are supported?**  
A: Currently RSA; more (ECC, Ed25519) are planned.

**Q: Where are my keys stored?**  
A: Keys are saved only where you choose. No automatic uploads or cloud storage.

**Q: How do I get help?**  
A: Use the Help menu or read the documentation in the docs/ folder.
