# Home-Automation
# 🏠 Home Automation System using ESP8266 and 4-Channel Relay

This project is a Wi-Fi-based Home Automation System using an **ESP8266 (NodeMCU)** microcontroller. It allows you to control **4 electrical appliances (represented by LED bulbs)** via a web interface or mobile app by toggling a **4-channel relay module**.

---

## 🚀 Features

- 🌐 Control 4 home appliances over Wi-Fi
- 📱 Access via web browser or IoT app (e.g. Blynk, custom dashboard)
- 💡 Real-time ON/OFF control of LED bulbs (can be replaced with real appliances)
- 🧠 Built on ESP8266 (NodeMCU) with relay module interface
- 🔌 Compact, low-cost, and easy to build

---

## 🧰 Hardware Components

| Component              | Quantity | Description                              |
|-----------------------|----------|------------------------------------------|
| ESP8266 NodeMCU        | 1        | Wi-Fi microcontroller board              |
| 4-Channel Relay Module | 1        | For switching 4 devices                  |
| LED Bulbs (AC or DC)   | 4        | Represents connected appliances          |
| Resistors (220Ω for LEDs) | 4     | For current limiting (if using DC LEDs)  |
| Power Supply (5V/USB)  | 1        | To power the ESP8266 and relays          |
| Jumper Wires & Breadboard | As needed | For connections                       |

---

## ⚙️ Circuit Connections

| ESP8266 Pin | Relay INx | Description               |
|-------------|-----------|---------------------------|
| D1 (GPIO5)  | IN1       | Controls Relay 1 (LED 1)  |
| D2 (GPIO4)  | IN2       | Controls Relay 2 (LED 2)  |
| D5 (GPIO14) | IN3       | Controls Relay 3 (LED 3)  |
| D6 (GPIO12) | IN4       | Controls Relay 4 (LED 4)  |
| GND         | GND       | Common Ground             |
| VIN or 5V   | VCC       | Power the Relay Module    |

**Relay Output:** Connect relay outputs to your LED bulbs or real AC appliances with proper insulation and safety.

---

## 💻 How It Works

1. ESP8266 hosts a simple web server or connects to an IoT app.
2. You open a browser or app and toggle switches.
3. The ESP8266 receives commands and activates relays.
4. Relays switch ON/OFF the LED bulbs (or appliances).

---

## 📦 Folder Structure


---

## 🖥️ Software Tools

- Arduino IDE (with ESP8266 board support installed)
- Libraries (if using web interface or Blynk):
  - `ESP8266WiFi`
  - `ESPAsyncWebServer` *(optional for async web control)*
  - `Blynk` *(if using Blynk IoT)*

---

## 📲 Optional Web Interface Example

Access IP address in browser:

```html
http://192.168.x.x
[ ON1 ] [ OFF1 ]
[ ON2 ] [ OFF2 ]
[ ON3 ] [ OFF3 ]
[ ON4 ] [ OFF4 ]

