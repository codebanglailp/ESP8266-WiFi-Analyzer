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
