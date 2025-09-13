---
lang: en
lang-niv: fonto
lang-ref: 022-jbk
layout: doc
order: 13
title: 'Weather'
---

# Weather App Documentation (v1.6.0)

Welcome to the Weather App documentation! This application provides real-time weather information and forecasts from multiple weather data providers.

## Features

- 🌦️ Current weather conditions with detailed metrics
- 📅 7-day weather forecast with hourly breakdowns
- 📖 Built-in Markdown documentation viewer
- 📊 Application log viewer for diagnostics
- 🌍 Multiple weather data providers
- 🌐 Multi-language support
- ⭐ Favorite locations with enhanced history
- ⚙️ Customizable settings and themes

## Recent Updates

For a detailed list of changes, see the [CHANGELOG.md](CHANGELOG.md) file.

## Getting Started

1. [Installation Guide](installation.md) - How to install and set up the application
2. [User Guide](usage.md) - How to use the application
3. [Configuration](configuration.md) - How to configure the application

## Advanced Topics

- [Weather Providers](providers.md) - Information about supported weather data providers
- [Translations](translations.md) - How to add or modify translations
- [Development Guide](development.md) - How to contribute to the project
- [Troubleshooting](troubleshooting.md) - Common issues and solutions

## Support

For support, please open an issue on our [GitHub repository](https://github.com/Nsfr750/weather).

## License

This project is licensed under the GPLv3 License - see the [LICENSE](https://github.com/Nsfr750/weather/blob/main/LICENSE) file for details.

# User Guide

## Getting Started

1. **Launch the Application**
   - Double-click the application icon or run from the command line
   - The main window will open with the default location's weather
   - On first run, you'll be guided through the initial setup

2. **Search for a Location**
   - Type a city name in the search box
   - Press Enter or click the search button (🔍)
   - For more accurate results, include the country code (e.g., "Paris, FR")
   - Right-click on the map to select a location

## Main Interface

### Weather Display

- **Current Weather**: Shows temperature, conditions, and additional details
  - Tap on any metric to toggle between units (e.g., °C/°F, km/h/mph)
  - Hover over icons for more information

- **7-Day Forecast**: Displays the weather forecast for the next 7 days
  - Click on a day to see hourly forecasts
  - Color-coded precipitation probability
  - Includes temperature ranges and weather conditions for each day

- **Weather Details**: Includes:
  - Feels like temperature
  - Humidity and dew point
  - Wind speed and direction
  - Pressure and visibility
  - UV index and air quality
  - Sunrise and sunset times

### Navigation

- **Search Bar**: Find weather for any location
  - Recent searches are saved automatically
  - Search by city name, ZIP code, or coordinates

- **Theme Toggle**: Switch between light, dark, or system theme

- **Menu Bar**: Access additional features and settings
  - File: New window, settings, quit
  - View: Toggle UI elements, refresh data, weather maps & radar
  - Favorites: Manage saved locations
  - Help: Documentation viewer, log viewer, about, check for updates

## Weather Maps & Radar

The Weather Maps & Radar feature provides interactive visualizations of weather patterns and conditions.

### Accessing Weather Maps

1. Click on **View** in the menu bar
2. Select **Weather Maps & Radar**
3. The Weather Maps dialog will open with multiple tabs

### Features

#### Radar Tab
- **Map Type**: Switch between different base maps (OpenStreetMap, OpenTopoMap, Stamen Terrain)
- **Layer**: Toggle between radar and satellite overlays
- **Search**: Find locations by name or coordinates

#### Temperature Tab
- View temperature variations across regions
- Toggle between Celsius and Fahrenheit
- Adjust the opacity of the temperature overlay

#### Precipitation Tab
- See current and forecasted precipitation
- Toggle between different precipitation layers
- View rain, snow, and other precipitation types

#### Wind Tab
- Visualize wind speed and direction
- Toggle wind barbs or streamlines
- Adjust the wind speed units (km/h, m/s, mph, knots)

### Using the Map
- **Zoom**: Use the mouse wheel or +/- buttons
- **Pan**: Click and drag the map
- **Search**: Enter a location in the search box and press Enter
- **Layers**: Toggle different weather layers using the controls
- **Fullscreen**: Click the fullscreen button for a larger view

### Tips
- The map will automatically center on your current location if location services are enabled
- Click on the map to get detailed weather information for that location
- Use the timeline controls to view forecast data for different times
- Right-click on the map to set a marker or get coordinates

## Features

### Favorites

- **Add to Favorites**: Click the star (☆) to save a location

- **View Favorites**: Access saved locations from the Favorites menu
  - Reorder favorites by drag and drop
  - Right-click for quick actions

- **Sync Favorites**: Enable cloud sync in settings

- **Remove from Favorites**: Click the filled star (★) to remove

### Settings

1. Click the gear icon (⚙️) or go to Menu > Settings
2. Configure options like:
   - **General**: Language, theme, units
   - **Weather**: Provider settings, update frequency
   - **Display**: Layout, animations, font size
   - **Notifications**: Weather alerts, rain alerts
   - **Advanced**: Cache, logging, developer options
3. Click "Save" to apply changes

### Command Line Interface

```bash
# Basic usage
weather-app [location] [options]

# Examples
weather-app "New York, US"
weather-app --provider openweathermap --units metric
weather-app --config ~/.config/weather/config.ini

# Options
  -h, --help            Show help message and exit
  -v, --version         Show version information
  -c, --config FILE     Specify configuration file
  -d, --debug           Enable debug mode
  --provider PROVIDER   Set weather provider
  --units {metric,imperial}
                        Set units system
  --lang LANG           Set language code
  --theme {light,dark,system}
                        Set color theme
  --no-gui              Run in console mode
```

## Keyboard Shortcuts

### Global Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + F` | Focus search bar |
| `Ctrl + ,` | Open Settings |
| `Ctrl + Q` | Quit Application |
| `F1` | Show Help |
| `Esc` | Close dialogs or clear search |
| `F5` | Refresh weather data |
| `Ctrl + R` | Refresh all data |
| `Ctrl + W` | Close current window |
| `Ctrl + N` | New window |

### Navigation Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Tab` | Switch between locations |
| `Ctrl + F` | Toggle favorites |
| `Ctrl + L` | Toggle location list |
| `Ctrl + M` | Toggle map view |

## Tips & Tricks

- **Right-click** on any weather card for quick actions
- **Double-click** the temperature to toggle between Celsius and Fahrenheit
- **Middle-click** on the map to set a custom location
- Use **mouse wheel** on the forecast to scroll through hours
- **Drag and drop** to reorder favorite locations
- **Pin** the window to stay on top of other applications
- Use **system tray** icon for quick access

### Documentation Viewer

- Access the built-in Markdown documentation from the Help menu
- Browse through comprehensive documentation
- Search functionality to find specific topics
- Zoom in/out for better readability
- Table of contents for easy navigation

### Log Viewer

- View application logs from the Help menu
- Filter logs by level (Debug, Info, Warning, Error)
- Search through log messages
- Copy logs to clipboard for troubleshooting

### Weather Maps
- Access weather maps from the View menu
- Interactive map with multiple layers:
  - Temperature
  - Precipitation
  - Wind speed
  - Cloud cover
- Pan and zoom to explore different regions
- Click on the map to get weather for that location

## Troubleshooting

If you encounter any issues:
1. Check your internet connection
2. Verify your API keys in Settings
3. Try switching to a different weather provider
4. Check the application logs for errors
5. Restart the application
6. Reset settings if needed

For additional help, please visit our [GitHub repository](https://github.com/Nsfr750/weather) or check the [Troubleshooting Guide](troubleshooting.md).

## Feedback

We welcome your feedback! Please let us know:
- What features you'd like to see
- Any bugs you encounter
- Your experience with the application

You can submit feedback through the application (Help > Send Feedback) or on our [GitHub Issues](https://github.com/Nsfr750/weather/issues) page.

# Troubleshooting Guide

This guide helps you resolve common issues you might encounter while using the Weather App.

## Table of Contents
- [Common Issues](#common-issues)
- [Log Files](#log-files)
- [Debugging](#debugging)
- [Performance Issues](#performance-issues)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Getting Help](#getting-help)

## Common Issues

### 1. Application Won't Start

**Symptoms**:
- The application crashes immediately after launch
- You see an error message about missing dependencies
- The application window doesn't appear

**Solutions**:
1. **Check System Requirements**:
   - Ensure you have Python 3.10 or higher installed
   - Verify all system dependencies are installed
   - Check disk space and permissions

2. **Reinstall Dependencies**:
   ```bash
   # Activate your virtual environment first
   pip install --upgrade -r requirements.txt
   ```

3. **Check for Conflicting Software**:
   - Temporarily disable antivirus/firewall
   - Close other applications that might be conflicting

4. **Reset Configuration**:
   ```bash
   # Backup your config first
   mv ~/.config/WeatherApp/config.ini ~/.config/WeatherApp/config.ini.bak
   ```

### 2. No Weather Data Displayed

**Symptoms**:
- The app opens but shows "No data available"
- Weather information doesn't update
- Location cannot be found

**Solutions**:
1. **Check Internet Connection**:
   - Verify your device is connected to the internet
   - Try accessing a website in your browser

2. **Verify API Keys**:
   - Check if your API key is valid and not expired
   - Ensure the API key has the correct permissions
   - Try regenerating the API key

3. **Provider Status**:
   - Check if the weather service is experiencing outages
   - Try switching to a different weather provider

4. **Location Services**:
   - Ensure location services are enabled
   - Try entering the location manually

### 3. High CPU or Memory Usage

**Symptoms**:
- The app becomes slow or unresponsive
- Your computer's fan runs loudly
- Other applications become slow

**Solutions**:
1. **Reduce Update Frequency**:
   - Increase the update interval in Settings > Weather
   - Disable automatic location updates if not needed

2. **Disable Animations**:
   - Go to Settings > Display
   - Toggle off "Enable animations"

3. **Clear Cache**:
   ```bash
   # Linux/macOS
   rm -rf ~/.cache/WeatherApp
   
   # Windows
   rmdir /s /q %LOCALAPPDATA%\WeatherApp\Cache
   ```

4. **Check for Memory Leaks**:
   - Monitor memory usage in Task Manager
   - Report any consistent memory growth

## Log Files

Log files contain detailed information about application events and errors. They are essential for troubleshooting.

### Log Locations

- **Linux/macOS**: `~/.local/share/WeatherApp/logs/`
- **Windows**: `%APPDATA%\WeatherApp\logs\`
- **macOS**: `~/Library/Logs/WeatherApp/`

### Log Levels

- **DEBUG**: Detailed information for debugging
- **INFO**: General application events
- **WARNING**: Potentially harmful situations
- **ERROR**: Errors that might still allow the app to continue
- **CRITICAL**: Severe errors that cause the app to crash

### Viewing Logs

1. **From the Application**:
   - Go to Help > View Logs
   - Filter by log level
   - Search for specific terms

2. **From Command Line**:
   ```bash
   # Linux/macOS
   tail -f ~/.local/share/WeatherApp/logs/app.log
   
   # Windows
   Get-Content -Path "$env:APPDATA\WeatherApp\logs\app.log" -Wait
   ```

## Debugging

### Enabling Debug Mode

1. **From Command Line**:
   ```bash
   python -m script.main --debug
   ```

2. **From Configuration**:
   ```ini
   [Logging]
   level = DEBUG
   ```

### Common Error Messages

#### "API Rate Limit Exceeded"
- **Cause**: Too many requests to the weather API
- **Solution**:
  - Wait before making more requests
  - Upgrade your API plan if needed
  - Implement proper caching

#### "Invalid API Key"
- **Cause**: The provided API key is invalid or expired
- **Solution**:
  - Verify the key is correct
  - Check for extra spaces
  - Generate a new key if needed

#### "Location Not Found"
- **Cause**: The specified location doesn't exist
- **Solution**:
  - Check for typos
  - Try a nearby larger city
  - Use coordinates instead of city name

### Using a Debugger

1. **VS Code**:
   - Set breakpoints in your code
   - Press F5 to start debugging
   - Use the debug console to inspect variables

2. **pdb (Python Debugger)**:
   ```python
   import pdb; pdb.set_trace()  # Add this line where you want to break
   ```

## Performance Issues

### Slow Startup

1. **Disable Unnecessary Plugins**:
   - Check for third-party plugins
   - Disable unused providers

2. **Optimize Imports**:
   - Use lazy loading for heavy modules
   - Remove unused imports

### High Memory Usage

1. **Check for Memory Leaks**:
   - Monitor memory usage over time
   - Look for objects that aren't being garbage collected

2. **Reduce Cache Size**:
   ```ini
   [Cache]
   max_size = 100  # MB
   ```

### Network Issues

1. **Check Connection**:
   ```bash
   ping api.openweathermap.org
   ```

2. **Proxy Settings**:
   - Configure proxy in Settings > Network
   - Check firewall settings

## Frequently Asked Questions

### Q: How do I update the application?
A: Use your package manager or download the latest version from GitHub.

### Q: Why is the weather data not updating?
A: Check your internet connection and API key. The app caches data to reduce API calls.

### Q: How do I change the temperature unit?
A: Go to Settings > Display > Units and select your preferred unit.

### Q: The app is using too much battery. What can I do?
A: Reduce the update frequency and disable unnecessary features like animations.

### Q: How do I report a bug?
A: Please open an issue on our [GitHub repository](https://github.com/Nsfr750/weather/issues) with detailed steps to reproduce the issue.

## Getting Help

If you've tried the solutions above and are still experiencing issues:

1. **Check the Documentation**:
   - [User Guide](usage.md)
   - [Configuration](configuration.md)
   - [API Documentation](api.md)

2. **Search Existing Issues**:
   - [GitHub Issues](https://github.com/Nsfr750/weather/issues)
   - [FAQ](https://github.com/Nsfr750/weather/wiki/FAQ)

3. **Ask the Community**:
   - [Discord](https://discord.gg/ryqNeuRYjD)
   - [GitHub Discussions](https://github.com/Nsfr750/weather/discussions)

4. **Contact Support**:
   - Email: nsfr750@yandex.com
   - Include your system information and error logs

### When Reporting an Issue

Please include the following information:
1. Weather App version
2. Operating System and version
3. Steps to reproduce the issue
4. Expected vs. actual behavior
5. Relevant error messages or logs
6. Screenshots if applicable

## Emergency Recovery

If the application becomes completely unresponsive:

1. **Force Quit**:
   - Windows: Ctrl+Alt+Delete → Task Manager → End Task
   - macOS: Command+Option+Esc → Force Quit
   - Linux: `pkill -f weather`

2. **Reset Configuration**:
   ```bash
   # Linux/macOS
   rm -rf ~/.config/WeatherApp
   
   # Windows
   rmdir /s /q %APPDATA%\WeatherApp
   ```

3. **Reinstall**:
   ```bash
   pip uninstall weather-app
   pip install --no-cache-dir weather-app
   ```

Remember to back up your configuration before making any changes!

# Translation Guide

This guide explains how to add or modify translations in the Weather App. The application uses a comprehensive translation system that supports multiple languages and right-to-left (RTL) text direction.

## Available Languages

The Weather App currently supports the following languages:

| Language | Code | Native Name | RTL | Status |
|----------|------|-------------|-----|--------|
| English | en   | English     | No  | Complete |
| Spanish | es   | Español     | No  | Complete |
| French  | fr   | Français    | No  | Complete |
| German  | de   | Deutsch     | No  | Complete |
| Italian | it   | Italiano    | No  | Complete |
| Portuguese | pt   | Português   | No  | Complete |
| Russian | ru   | Русский     | No  | Complete |
| Japanese | ja   | 日本語      | No  | Complete |
| Korean  | ko   | 한국어      | No  | Complete |
| Arabic  | ar   | اَلْعَرَبِيَّةُ | Yes | Complete |
| Hebrew  | he   | עברית      | Yes | Complete |
| Hungarian | hu  | Magyar      | No  | Complete |
| Polish  | pl   | Polski      | No  | Complete |
| Turkish | tr   | Türkçe      | No  | Complete |
| Dutch   | nl   | Nederlands  | No  | Complete |
| Chinese (Simplified) | zh | 简体中文   | No  | Complete |

## Language Menu Implementation

The language menu automatically displays available languages using the following logic:

1. It first tries to load language names from the current UI language's translation file
2. If not found, it falls back to English names
3. As a last resort, it uses a built-in dictionary of common language names

### Language Name Keys

Each translation file should include language names for all supported languages using the pattern `language_XX` where `XX` is the language code. For example:

- `language_en`: "English"
- `language_es": "Español"
- `language_fr": "Français"

### Menu Text

Each translation file should also include these UI-specific keys:

- `language_menu`: The menu title (e.g., "Language")
- `language_tip`: Tooltip text for the language menu

## Translation System

The translation system is based on JSON files and includes these features:

- String interpolation with variables
- Right-to-left (RTL) language support
- Fallback to English for missing translations
- Dynamic language switching without app restart
- Optimized loading with translation memory

### File Structure

```text
lang/
├── __init__.py
├── language_manager.py    # Core translation management
└── translations/
    ├── en.json           # English (base language)
    ├── it.json           # Italian
    ├── es.json           # Spanish
    ├── fr.json           # French
    ├── de.json           # German
    ├── pt.json           # Portuguese
    ├── ru.json           # Russian
    ├── ja.json           # Japanese
    ├── ko.json           # Korean
    ├── zh.json           # Chinese (Simplified)
    ├── ar.json           # Arabic (RTL)
    ├── he.json           # Hebrew (RTL)
    ├── hu.json           # Hungarian
    ├── pl.json           # Polish
    ├── tr.json           # Turkish
    └── nl.json           # Dutch
```

## Adding a New Language

### Adding a New Language

To add a new language:

1. Add a new JSON file in `lang/translations/` with the language code (e.g., `fr.json` for French)
2. Copy all keys from `en.json`
3. Translate all values to the target language
4. Add the language name in its own language (e.g., `"language_fr": "Français"`)
5. Add the language to the language menu by including these keys:
   - `language_menu`: The menu title (e.g., "Language")
   - `language_tip`: Tooltip text for the language menu (e.g., "Select application language")

Example for French (`fr.json`):
```json
{
  "language_menu": "&Langue",
  "language_tip": "Sélectionner la langue de l'application",
  "language_fr": "Français",
  "language_en": "Anglais",
  "language_es": "Espagnol"
  // ... other translations
}
```

## Best Practices

1. **Consistency**
   - Use consistent terminology throughout the app
   - Maintain the same tone and style
   - Follow the language's standard date/time/number formats

2. **Variables**
   - Use `{variable}` syntax for dynamic content
   - Keep variables in the same position as the source language when possible
   - Document expected variable types and formats

3. **Pluralization**
   - Use the `_plural` key for plural forms
   - Follow the language's plural rules

   ```python
   {
       'hour': '{count} hour',
       'hour_plural': '{count} hours',
       'minute': '{count} minute',
       'minute_plural': '{count} minutes',
   }
   ```

4. **Special Characters**
   - Use proper Unicode characters for accented letters and symbols
   - Ensure proper encoding (UTF-8)
   - Test special characters on all platforms

5. **Length Considerations**
   - Account for text expansion (some languages are 30-40% longer than English)
   - Keep UI elements flexible to accommodate different text lengths
   - Test UI with the longest translations

## Right-to-Left (RTL) Support

For RTL languages like Arabic and Hebrew:

1. Set `is_rtl = True` in the language configuration
2. The application will automatically:
   - Mirror the UI layout
   - Set text alignment to right
   - Adjust scrollbars and other UI elements

## Testing Translations

1. **Visual Testing**
   - Check for text overflow
   - Verify proper alignment
   - Test with different font sizes

2. **Functional Testing**
   - Test all UI elements with the target language
   - Verify date, time, and number formatting
   - Check RTL support if applicable

3. **Automated Tests**
   - Run the test suite with the new language
   - Check for missing translations
   - Verify variable substitution

## Contributing Translations

1. Fork the repository
2. Create a new branch for your translation
3. Add or update the translation files
4. Submit a pull request with a clear description

## Troubleshooting

### Common Issues

- **Missing Translations**: Fall back to English
- **Text Overflow**: Adjust UI elements or shorten translations
- **Special Characters**: Ensure proper encoding and font support

## Getting Help

For translation issues, please open an issue on our [GitHub repository](https://github.com/yourusername/weather-app/issues).
1. Join our [Discord](https://discord.gg/ryqNeuRYjD)
2. Contact the maintainers
