# 📡 ESP8266 WiFi Analyzer (Advanced Version)

> A Production-Grade Offline WiFi Analysis Tool for ESP8266  
> Real-Time Network Scanner • Channel Analyzer • OLED Monitor

---

![Platform](https://img.shields.io/badge/Platform-ESP8266-blue)
![Type](https://img.shields.io/badge/Type-WiFi%20Analyzer-green)
![License](https://img.shields.io/badge/License-MIT-orange)
![Version](https://img.shields.io/badge/Version-1.0.0-red)

---

## 🚀 Overview

**ESP8266 WiFi Analyzer** transforms your ESP8266 into a powerful offline network diagnostic tool.

No internet required.  
Just connect to the ESP Access Point and open the dashboard in your browser.

This firmware provides:

- 📡 Real-time WiFi network scanning
- 📊 Signal strength (RSSI) visualization
- 📶 Channel usage analysis (1–13)
- 🧠 Automatic best channel suggestion
- 📈 Animated signal bar dashboard
- 📺 OLED live monitoring display
- ⚡ Non-blocking background scan engine

---

## 🧠 How It Works

1. ESP8266 starts in **Access Point mode**
2. User connects to the device WiFi
3. Open `192.168.4.1`
4. Dashboard loads from **LittleFS**
5. WiFi scan results are returned via JSON API
6. OLED shows live network statistics

---

## 📂 Project Structure

```

ESP8266-WiFi-Analyzer/
│
├── WiFi_Analyzer.ino
└── data/
└── index.html

```

Only **2 files required**.

---

## 📊 Core Features

### 📡 WiFi Network Scanner

- SSID
- RSSI (Signal Strength)
- Signal Quality (%)
- Channel
- Encryption Type
- BSSID (MAC Address)

---

### 📶 Channel Usage Analyzer

- Counts networks per channel (1–13)
- Displays usage bar chart
- Suggests best available channel
- Helps reduce WiFi interference

---

### 📈 Signal Quality Calculation

Signal percentage calculated from RSSI:

```

If RSSI <= -100 → 0%
If RSSI >= -50 → 100%
Else → 2 × (RSSI + 100)

```

---

### 📺 OLED Display (128x64)

Live display includes:

- Device Name
- IP Address
- Total Networks Found
- Strongest Signal
- Best Channel Suggestion
- Scan Status

Professional splash screen on boot.

---

## 🌐 Web Dashboard

Premium Dark Network Tool UI:

- Modern gradient header
- Animated signal bars
- Channel usage graph
- Auto-refresh system
- Responsive design
- Smooth transitions
- Loading indicators

### 🎨 Color Palette

| Element       | Color       |
| ------------- | ----------- |
| Background    | #0f172a     |
| Card          | #1e293b     |
| Accent        | Blue / Cyan |
| Strong Signal | Green       |
| Medium Signal | Yellow      |
| Weak Signal   | Red         |

---

## ⚙️ API Endpoints

| Endpoint        | Method | Description         |
| --------------- | ------ | ------------------- |
| `/api/scan`     | GET    | WiFi scan results   |
| `/api/channels` | GET    | Channel usage stats |
| `/api/status`   | GET    | Device status info  |
| `/api/restart`  | POST   | Restart device      |

All responses are structured JSON.

---

## 🔧 Default Configuration

| Setting       | Value        |
| ------------- | ------------ |
| Mode          | Access Point |
| Default IP    | 192.168.4.1  |
| Scan Mode     | Non-blocking |
| Channel Range | 1–13         |

---

## 🧰 Required Libraries

Install in Arduino IDE:

- ESP8266WiFi
- ESP8266WebServer
- LittleFS
- ArduinoJson
- Adafruit SSD1306
- Adafruit GFX

---

## 🚀 Installation Guide

### 1️⃣ Upload Frontend

- Place `index.html` inside `/data`
- Use **LittleFS Data Upload Tool**

### 2️⃣ Flash Firmware

- Open `WiFi_Analyzer.ino`
- Select board (NodeMCU / D1 Mini)
- Upload

### 3️⃣ Connect

- Connect to device WiFi
- Open browser → `192.168.4.1`

---

## 🛡 Performance Optimized

- No blocking `delay()`
- Background async scan engine
- Controlled JSON buffer size
- Limited network result handling
- Clean modular structure

---

## 🧪 Tested On

- NodeMCU ESP8266
- LOLIN D1 Mini
- ESP8266MOD

---

## 🛣 Roadmap

- WebSocket real-time push updates
- Export scan results (JSON)
- Interference heatmap
- Authentication system
- OTA firmware update
- Network logging system

---

## 📜 License

MIT License – Free to use, modify, and distribute.

---

## 👨‍💻 Author

**CODE Bangla ILP**  
Embedded Systems & IoT Development

GitHub: https://github.com/codebanglailp

---

⭐ If you find this project useful, consider giving it a star!
