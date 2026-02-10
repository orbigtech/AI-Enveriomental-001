# AI-Enveriomental-001 — BME688 + BME280 Environmental Sensor Breakout (Qwiic/Grove)

A compact and practical **environmental sensing breakout** that combines:
- **BME688** — indoor air quality sensor (VOC, eCO₂ estimation, AQI)
- **BME280** — temperature, humidity, barometric pressure

Built for makers: **plug-and-play I²C** via **Qwiic / Grove**, plus classic header pins for the old-school reliable way of wiring.

---

## Why this board exists

Most maker projects need a **simple, repeatable** environmental sensor block:
- Air quality trends (VOC / eCO₂ estimation / AQI)
- Temperature / humidity / pressure as baseline context
- A single breakout that is easy to deploy in prototypes, demos, and small product runs

This board keeps it **modular, low friction, and easy to integrate**.

---

## Features

- **BME688** (VOC / eCO₂ / AQI)
- **BME280** (T / RH / Pressure)
- **I²C** interface (shared bus)
- **Qwiic + Grove** connectors for fast wiring
- Header pins for traditional wiring
- Compact form factor for enclosures and tight builds
- Repo includes: **schematic, PCB, BOM, fabrication files, examples**

---

## Supported Platforms

- **Arduino** (UNO / Nano / Mega / R4 / etc.) with 3.3V I²C level compatibility
- **ESP32** (recommended for IoT)
- **Raspberry Pi** (I²C via GPIO)

> Tip: If your host board uses **5V I²C**, use a proper level shifter unless your design already guarantees 3.3V-safe lines.

---

## Interface & Pinout

### I²C Signals
- **SDA**
- **SCL**
- **3V3**
- **GND**

### Default I²C Addresses (typical)
- **BME280**: `0x76` or `0x77` (depends on SDO strap)
- **BME688**: commonly `0x53` (verify in your scan)

> Always run an I²C scanner first. It saves time and avoids guessing.

---

## Getting Started

### 1) Hardware
1. Connect via **Qwiic** or **Grove**, or use headers:
   - 3V3 → 3.3V
   - GND → GND
   - SDA → SDA
   - SCL → SCL
2. Power up the system.

### 2) Quick I²C Scan (Arduino)
Use a standard I²C scanner sketch and confirm both devices appear.

### 3) Libraries
Recommended approach:
- Use a proven **BME280** library (Adafruit / Bosch-based)
- Use a compatible **BME688** library (vendor/community)

This repo provides example code paths for both.

---

## Repository Structure


