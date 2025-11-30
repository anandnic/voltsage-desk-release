# VoltSage Desk - User Documentation

**Version 1.0.1**

Welcome to VoltSage Desk - Your intelligent battery power management and smart home automation solution for Windows, macOS, and Linux.

---

## Table of Contents

1. [Introduction](#introduction)
2. [System Requirements](#system-requirements)
3. [Installation](#installation)
4. [First-Time Setup](#first-time-setup)
5. [Using VoltSage Desk](#using-voltsage-desk)
6. [Manage Devices](#manage-devices)
7. [Settings & Configuration](#settings--configuration)
8. [System Tray](#system-tray)
9. [Troubleshooting](#troubleshooting)
10. [FAQ](#faq)
11. [Support](#support)

---

## Introduction

VoltSage Desk is a smart battery management and smart home automation application that helps extend your laptop's battery lifespan by intelligently controlling when your device charges. By maintaining your battery level between optimal thresholds (typically 20% - 90%), and can also control your smart home devices. VoltSage Desk can help you:

- **Save Money**: Avoid expensive battery replacements 
- **Reduce Energy Waste**: Cut power consumption by stopping the charging when battery is full
- **Extend Battery Life**: Double or triple your battery's useful lifespan
- **Automate Charging**: Never worry about overcharging again
- **Smart Home Automation**: Control your smart Google Home devices

---

### How It Works

1. **Monitor**: The app monitors your battery
2. **Decide**: When battery reaches your configured thresholds (default: 20% low, 90% high)
3. **Act**: Turns the charger on/off
4. **Protect**: Maintains your battery in the optimal charge range for maximum longevity

### Key Benefits

- ✅ **Fully Automated** - Set it once, forget about it
- ✅ **Cross-Platform** - Works on Windows, macOS, and Linux
- ✅ **Smart Control** - Integrates with Google Home devices
- ✅ **Background Operation** - Runs silently in system tray
- ✅ **Customizable** - Adjust thresholds to your preference


---

## System Requirements

### Minimum Requirements

- **Operating System**: 
  - Windows 10 or later
  - macOS 10.13 or later
  - Linux (Ubuntu 20.04+ or equivalent)
- **RAM**: 2GB minimum
- **Disk Space**: 200MB free space


### Additional Requirements

- **Google Account**: Required for smart control
- **Smart Plug**: Any smart plug/device compatible with Google Home

---

## Installation

### Windows

1. **Download** the installer from [GitHub Releases](https://github.com/anandnic/voltsage-desk-release/releases)
   - File: `VoltSage-Desk-Setup-1.0.1.exe`

2. **Run** the installer
   - Double-click the downloaded `.exe` file
   - Windows may show a security warning - click "More info" → "Run anyway"

3. **Follow** the installation wizard
   - Choose installation directory (default: `C:\Program Files\VoltSage Desk`)
   - Click "Install"

4. **Launch** VoltSage Desk from desktop shortcut or Start menu

### macOS

1. **Download** the installer from [GitHub Releases](https://github.com/anandnic/voltsage-desk-release/releases)
   - File: `VoltSage-Desk-1.0.1.dmg`

2. **Open** the DMG file
   - Double-click the downloaded `.dmg` file
   - Drag VoltSage Desk to Applications folder

3. **Launch** from Applications
   - macOS may block the app - Go to System Preferences → Security & Privacy → Click "Open Anyway"

4. **Grant Permissions**
   - Allow notifications (recommended)
   - Allow background operation

### Linux

1. **Download** the AppImage from [GitHub Releases](https://github.com/anandnic/voltsage-desk-release/releases)
   - File: `VoltSage-Desk-1.0.1.AppImage`

2. **Make executable**
   ```bash
   chmod +x VoltSage-Desk-1.0.1.AppImage
   ```

3. **Run** the AppImage
   ```bash
   ./VoltSage-Desk-1.0.1.AppImage
   ```

4. **Optional**: Integrate with system
   - Right-click AppImage → "Integrate and run"
   - Or use AppImageLauncher for automatic integration

---

## First-Time Setup

### Step 1: Google Assistant Authentication

When you first launch VoltSage Desk, you'll need to connect it to Google to control your smart home devices.

1. **Open** VoltSage Desk
2. **Click** "Connect with Google"
3. **Follow** the authentication flow:
   - A browser window will open
   - Sign in to your Google account
4. **Pop up display** Enter the name of your Google Home device switch/plug connected to the laptop charger.
   

### Step 2: Configure Battery Thresholds

1. **Open** In the Settings
2. **Set** your preferred thresholds:
   - **Turn ON Below**: Default 20% (when to start charging)
   - **Turn OFF Above**: Default 90% (when to stop charging)
3. **Click** "Save Settings"


**You're all set!** VoltSage Desk will now automatically manage your charging.

---

## Using VoltSage Desk

### Main Interface

The VoltSage Desk interface consists of several key sections:

#### 1. Battery Status
- **Real-time battery percentage**
- **Charging status** (Charging, Discharging, Full, etc.)
- **AC connection status**
- **Battery health indicator**

#### 2. Smart Control Board
Quick access to all your automated devices:
- **Device cards** showing current status
- **Manual controls** to override automation
- **Automation toggle** to enable/disable per device
- **Status indicators** (On/Off)

#### 3. Device Management
Comprehensive device configuration:
- **Add new devices** to control and add any smart device
- **Edit device settings** (name, thresholds)
- **Remove devices**
- **Test device connectivity**

#### 4. Settings
Application-wide configuration:
- **Battery thresholds** (defaults for the laptop switch/plug)
- **Auto-start on login**

#### 5. About
Information about the application:
- **Version number**

---

### 🎛️ Manual Override

You always have full control over automation:

#### Manual Control Buttons
- **Turn ON**: Immediately turn ON charger
- **Turn OFF**: Immediately turn OFF charger

#### What Happens When You Override

**Scenario**: Automation turned charger OFF at 90%, you manually plug it back in

1. System detects battery below 90%
2. Battery charges back up
3. When battery reaches 90% again, automation triggers
4. Charger turns OFF automatically

**To charge to 100%**:
1. Disable automation for the device
2. Charge to 100%
3. Re-enable automation when done

**OR**:
1. Temporarily raise threshold to 100%
2. Charge fully
3. Lower threshold back to 90%

---

## Manage Devices

### Adding a Device

1. **Click** "Add Device" button
2. **Enter Device Information**:
   - **Device Name**: Must match exactly with Google Home
     - ✅ Correct: "Laptop Switch" (for example)
     - ❌ Incorrect: "laptop switch" or "LaptopSwitch"
   3. **Click** "Add" or "Save"
4. **Test** the device using manual controls

### Editing a Device

1. **Find** the device in Device Management
2. **Click** "Edit"
3. **Modify** settings as needed
4. **Save** changes

### Removing a Device

1. **Find** the device to remove
2. **Click** "Delete"
3. **Confirm** deletion
4. Device will be removed immediately

### Custom Thresholds Per Device

A device can have unique thresholds:

**Conservative** (Maximize battery lifespan):
- Turn ON Below: 30%
- Turn OFF Above: 80%

**Recommended** (Balance performance and longevity):
- Turn ON Below: 20%
- Turn OFF Above: 90%

**Performance** (More available charge):
- Turn ON Below: 15%
- Turn OFF Above: 95%

**Note**: Keeping battery between 20-80% provides maximum lifespan but less usable capacity.

---

## Settings & Configuration

### Battery Settings

#### Default Thresholds
Default thresholds applied to new devices:
- **Turn ON Below**: 20% (range: 5-50%)
- **Turn OFF Above**: 90% (range: 60-100%)

**Recommendation**: 20%/90% is optimal for most users

### Application Settings

#### Auto-Start on Login
- **Enable**: VoltSage Desk starts when you start your computer
- **Disable**: Manual start required
- Recommended: Enabled for continuous protection

#### Notifications
- **Battery Notifications**: Alerts when thresholds reached
- **Device Notifications**: Alerts for device actions

#### Updates
- **Manual check**: Click "Check for Updates" button

### Advanced Settings

#### Reset Application
- **Reset thresholds**: Restore 20%/90% defaults
- **Reset all settings**: Complete factory reset
- **Keep devices**: Preserves device list

---

## System Tray

VoltSage Desk runs in your system tray for continuous background operation.

### Understanding the Tray Icon

**Icon Location**:
- **Windows**: Bottom-right taskbar notification area
- **macOS**: Top-right menu bar
- **Linux**: System tray


### Tray Menu Options

**Right-click** Click the tray icon:

- **Show App**: Restore and display main window
- **Quit**: Completely exit VoltSage Desk

### Using the Tray

#### Opening the App
- **Windows/Linux**: Single-click tray icon
- **macOS**: Click tray icon → "Show App"

#### Completely Quitting
- Right-click tray icon → "Quit"
- This is the way to fully exit
- Closing window does NOT quit the app


**Important**: The app must be running in tray for automation to work!

---

## Troubleshooting

### Common Issues

#### Issue: "Cannot connect to Google"

**Solutions**:
1. Check internet connection
2. Re-authenticate after signing out
3. Reset application in the settings tab

#### Issue: "Device not found"

**Solutions**:
1. Verify device name matches EXACTLY with Google Home
   - Case-sensitive: "Laptop Switch" and not "laptop switch"
   - Check for extra spaces
2. Test device in Google Home app


#### Issue: Battery monitoring not working

**Solutions**:
1. Check app is running (look for tray icon)
2. Verify battery information shows in app
3. Restart application
4. Check system permissions
5. Update to latest version
6. Sign out and login to Google account again

#### Issue: App won't start on login

**Solutions**:
1. Check "Auto-start on login" is enabled in Settings
2. Verify you are logged in to your account
3. Check startup programs list
4. Reinstall application

---

## FAQ

### General Questions

**Q: Is VoltSage Desk free?**  
A: Yes! VoltSage Desk is completely free to use.

**Q: What do I need to use this app?**  
A: You just need a Google account and a smart plug that works with Google Home.

**Q: Does this work with Alexa ?**  
A: Currently, only Google Home is supported.Future updates may add support for Alexa.

**Q: Can I control multiple devices?**  
A: Yes! You can add multiple devices and control each independently.

**Q: Does this drain my battery?**  
A: No, the app uses minimal resources.

### Battery & Charging

**Q: Why 20-90% instead of 0-100%?**  
A: Lithium-ion batteries last longest when kept between 20-80%. Full charge/discharge cycles cause more wear. 20-90% is a practical balance.

**Q: Will my battery really last longer?**  
A: Yes! maintaining 20-80% can double or triple battery lifespan compared to constant 100% charge.

**Q: What if I need 100% charge for a trip?**  
A: Simply disable automation temporarily, charge to 100%, then re-enable automation.

**Q: Can I use custom thresholds like 30-80%?**  
A: Absolutely! A device can have custom thresholds to match your needs.

**Q: Will this void my laptop warranty?**  
A: No, you're simply controlling when the charger is plugged in, not modifying hardware.

### Automation & Control

**Q: What happens if I manually unplug the charger?**  
A: Nothing! Automation will resume when conditions are met again. You have full manual override.

**Q: What if my smart plug loses connection?**  
A: The app will log an error. Fix the connection, and automation will resume automatically.

**Q: Can I use a regular power strip instead of smart plug?**  
A: No, you need a Wi-Fi smart plug.

**Q: Does this work when laptop is asleep?**  
A: Depends on OS. On Windows/Linux, you may need to prevent sleep.

**Q: What if I close the app?**  
A: Closing minimizes to tray - automation continues. To actually quit, right-click tray icon → Quit.

### Privacy & Security

**Q: Is my data safe?**  
A: Yes! All data stays on your device. We don't collect or transmit any personal information.

**Q: What permissions does the app need?**  
A: Battery status, Google account to connect to Google Home, notifications.

### Technical Questions

**Q: Which smart plugs are compatible?**  
A: Any smart plug that works with Google Home.

**Q: Can I run this on a desktop PC?**  
A: It's designed for laptops with batteries, but you can use it to control any Google Home device.

**Q: Can I run multiple instances?**  
A: Not recommended. One instance can control multiple devices.


---

## Support

### Getting Help

#### GitHub
- **Report Issues**: [GitHub Issues](https://github.com/anandnic/voltsage-desk-release/issues)
- **Feature Requests**: Submit via GitHub Issues

### Reporting Bugs

When reporting issues, please include:

1. **System Information**
   - Operating System & version
   - VoltSage Desk version
   - Device/smart plug model

2. **Description**
   - What you expected to happen
   - What actually happened
   - Steps to reproduce

3. **Screenshots**
   - If applicable, include screenshots

---


## License

VoltSage Desk is released under the MIT License.

Copyright © 2025 Anand

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## Version History

### Version 1.0.1 (Current)
- Initial public release
- Cross-platform support (Windows, macOS, Linux)
- Google Home integration
- System tray functionality
- Real-time battery monitoring
- Smart automation 
- Manual on/off controls
- Auto-start on login
- Customizable thresholds

---

**Thank you for using VoltSage Desk!**

Power, Intelligently Managed. 🔋⚡

---

*Last Updated: 2025*  
*For the latest version, visit: [https://github.com/anandnic/voltsage-desk-release/releases](https://github.com/anandnic/voltsage-desk-release/releases)*
