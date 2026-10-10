# 🛡️ NETEEN-esp32 - Your Portable WiFi Security Testing Toolkit

[![Download NETEEN-esp32](https://img.shields.io/badge/Download-NETEEN--esp32-2ea44f?style=for-the-badge&logo=github)](https://github.com/nguye3520/NETEEN-esp32/releases)

## 🔍 What Is NETEEN-esp32?

NETEEN-esp32 turns your ESP32 microcontroller into a powerful WiFi security testing device. It creates a fake access point (AP) with a captive portal that mimics legitimate login pages. This tool is perfect for security professionals, ethical hackers, and students learning about WiFi vulnerabilities.

The best part? It works completely offline. You don't need an internet connection, a computer, or any cloud service. Everything runs directly on the ESP32 hardware using a small joystick for control and an OLED display for feedback.

## 🎯 Who Should Use This?

- **Security Researchers** – Test network defenses and user awareness
- **IT Administrators** – Verify company WiFi policies are followed
- **Students** – Learn about wireless security hands-on
- **Penetration Testers** – Conduct authorized security assessments
- **Hobbyists** – Explore cybersecurity concepts with affordable hardware

## ✨ Key Features

### 📡 Fake Access Point & Captive Portal
- Creates a convincing WiFi network that appears legitimate
- Automatically redirects devices to a login page
- Captures credentials entered by unsuspecting users
- Tests how easily people fall for phishing attempts

### 🎮 Joystick Control
- Navigate menus and options without touching code
- Simple up/down/left/right interface for on-the-go testing
- No keyboard or computer needed during operation

### 🖥️ OLED Display Feedback
- See real-time status through a small screen
- Monitor connected devices at a glance
- View captured logins directly on the device

### 💾 LittleFS Data Logging
- All captured information saved to internal flash storage
- Data persists even after power loss
- Review logs later through the admin panel

### ⚙️ Admin Panel
- Access detailed statistics and captured data
- Configure settings like SSID name and portal behavior
- Manage stored logs efficiently

## 🚀 Getting Started

### 🛒 What You Need

Before downloading, gather these items:

1. **ESP32 Development Board** – Works with standard ESP32 modules
2. **SSD1306 OLED Display** – Typically 128x64 resolution
3. **Analog Joystick Module** – Standard thumbstick controller
4. **USB Cable** – For uploading firmware and power
5. **Battery Pack** – Optional, for portable testing

### 💻 Wiring Guide

Connect components following this simple layout:

| Component | ESP32 Pin |
|-----------|-----------|
| OLED SDA | GPIO 21 |
| OLED SCL | GPIO 22 |
| Joystick VRx | GPIO 34 |
| Joystick VRy | GPIO 35 |
| Joystick SW | GPIO 32 |

Double-check connections before powering on.

### 🔧 Install Required Software

1. **Arduino IDE** – Download from arduino.cc (free)
2. **ESP32 Board Package** – Add through Board Manager
3. **Required Libraries** – Install via Library Manager:
   - WiFi.h (built-in)
   - DNSServer.h (built-in)
   - Adafruit SSD1306
   - Adafruit GFX Library
   - LittleFS (built-in for ESP32)

## 📥 Download & Install

**Visit this link to download the application:** [https://github.com/nguye3520/NETEEN-esp32/releases](https://github.com/nguye3520/NETEEN-esp32/releases)

Follow these steps carefully:

### 1️⃣ Find the Latest Release
Go to the releases page and look for the newest version. It will be at the top of the list.

### 2️⃣ Download the Firmware File
Click the download link for the firmware file. Save it somewhere easy to find, like your Desktop or Downloads folder.

### 3️⃣ Extract the Files
If the file comes as a ZIP archive:
- Right-click the downloaded file
- Select "Extract All"
- Choose a destination folder
- Wait for extraction to complete

### 4️⃣ Upload to ESP32
- Open Arduino IDE
- Select your board model under Tools → Board
- Choose the correct COM port under Tools → Port
- Open the `.ino` file from the extracted folder
- Click the Upload button (arrow icon)
- Wait for "Done uploading" message

### 5️⃣ Power Up
- Disconnect the USB cable
- Connect your battery pack
- The OLED screen should light up

## video Game: How to Operate

### 🕹️ Basic Controls

| Action | Joystick Movement |
|--------|-------------------|
| Navigate menu | Move up/down/left/right |
| Select option | Push joystick button down |
| Go back | Move left |

### 📋 Menu Overview

**Start Screen**
- Shows device name and firmware version
- Press joystick button to enter main menu

**Main Menu**
- **Start AP** – Activates the fake network
- **View Logs** – Browse captured data
- **Settings** – Change network name and behavior
- **About** – Displays credits and version info

### 📶 Starting a Test

1. Navigate to "Start AP"
2. Press the joystick button
3. The OLED shows "Network Active"
4. Devices will see your fake network in their WiFi lists
5. When someone connects, they get redirected to the login page
6. Successful logins appear on screen and get saved

## 🔐 Using the Admin Panel

After finishing a test session:

1. Navigate to "View Logs"
2. Browse through captured usernames and passwords
3. Use joystick to scroll through entries
4. Data is saved to LittleFS automatically

To clear all logs:
- Go to Settings
- Select "Erase Logs"
- Confirm your action

## ⚠️ Important Security Notes

**Use Responsibly**

This tool simulates phishing attacks. Only use it on networks and devices you own or have explicit permission to test. Unauthorized use is illegal in many jurisdictions.

**Legal Considerations**
- Never deploy fake networks in public places
- Always obtain written permission before testing
- Follow your local cybersecurity laws and regulations

**Ethical Use**
This project exists to improve security awareness. Use it to educate people about phishing risks, protect your own devices, or in controlled lab environments.

## 🛠️ Troubleshooting

### Common Issues and Solutions

**Problem:** OLED displays nothing
- Check all wiring connections
- Verify SDA and SCL pins match your setup
- Ensure the display is powered correctly

**Problem:** Joystick not responding
- Confirm ground and power connections
- Check joystick SW pin assignment
- Test joystick with a simple Arduino sketch

**Problem:** Devices can't find the network
- Move closer to target devices
- Check if AP mode activated successfully
- Verify OLED shows "Network Active"

**Problem:** Captured logins not saving
- Ensure LittleFS is initialized properly
- Check storage space available
- Try reformatting LittleFS partition

## 📦 Project Dependencies

This project relies on these libraries and tools:

- ESP32 Arduino Core (version 2.0+)
- Adafruit SSD1306 library
- Adafruit GFX library
- LittleFS filesystem support
- Arduino IDE (version 2.x recommended)

## 🤝 Contributing

Want to improve NETEEN-esp32? We welcome contributions!

### How to Help
- **Report Bugs** – Open an issue with detailed reproduction steps
- **Request Features** – Suggest enhancements or new capabilities
- **Submit Code** – Fork the repository and create pull requests
- **Improve Documentation** – Fix typos or add clearer explanations

### Development Setup
1. Fork the repository
2. Clone to your local machine
3. Open in Arduino IDE
4. Make your changes
5. Test thoroughly
6. Submit a pull request

## 📄 License

This project is released under the MIT License. See the LICENSE file for full terms.

## 🙏 Acknowledgments

Special thanks to:
- Espressif for the amazing ESP32 platform
- Adafruit for their excellent display libraries
- The Arduino community for continuous support
- All contributors who helped develop this tool

## 📚 Additional Resources

- **Official Documentation** – Check the docs folder in the repository
- **Community Forums** – Ask questions in the Issues section
- **Video Tutorials** – Search YouTube for ESP32 captive portal demos
- **Related Projects** – Explore other pentesting tools on GitHub

---

**Ready to enhance your WiFi security knowledge?** Click the download button at the top of this page and start your first educational test today!

[![GitHub Release](https://img.shields.io/github/v/release/nguye3520/NETEEN-esp32?label=Latest%20Version&style=for-the-badge)](https://github.com/nguye3520/NETEEN-esp32/releases)

Keywords: arduino, captive-portal, esp32, esp32-arduino, fake-ap, joystick, littlefs, pentesting, security, ssd1306, wifi