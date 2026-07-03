# JustBeatIt


Below is a professional **README.md** for your **Zen Sync** project that you can include in your GitHub repository and send to manufacturers together with your schematic and PCB files.

---

````markdown
# 🎹 Zen Sync
### Heartbeat-Controlled Music Synthesizer

> Transform your heartbeat into immersive ambient music.

![Version](https://img.shields.io/badge/version-v1.0-blue)
![Prototype](https://img.shields.io/badge/status-Prototype-orange)
![Platform](https://img.shields.io/badge/ESP32-S3-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

# Overview

Zen Sync is a portable handheld music instrument that combines:

- ❤️ Real-time ECG heartbeat sensing
- 🎹 Piano keyboard synthesizer
- 🎵 HiChord-style chord engine
- 🎧 Headphone audio output
- 📱 Touchscreen interface (LVGL)
- 📡 WiFi & Bluetooth
- 🎼 Pocket Operator synchronization

Unlike traditional synthesizers, Zen Sync allows the user's heartbeat to become part of the musical experience.

This project is intended for:

- Meditation
- Ambient music
- Live performance
- Biofeedback experiments
- Music education

**Not intended for medical diagnosis.**

---

# Features

✔ Real-time ECG waveform

✔ Heart Rate (BPM)

✔ Heartbeat frequency

✔ Touch Piano Keyboard

✔ Chord Generator

✔ I2S Audio

✔ Headphone Output

✔ Pocket Operator Sync

✔ WiFi

✔ Bluetooth

✔ Rechargeable Battery

✔ USB-C Charging

---

# Hardware Architecture

```
ECG Electrodes
      │
      ▼
 AD8232 ECG Module
      │
      ▼
 ESP32 Smart Display
 (Touch + WiFi + Bluetooth)
      │
 ┌────┼───────────────┐
 │    │               │
 ▼    ▼               ▼
LCD  ECG Engine   Piano Engine
 │
 ▼
Audio Engine
 │
 ▼
PCM5102 DAC
 │
 ▼
Headphones
```

---

# Main Components

| Component | Description |
|------------|-------------|
| ESP32 Smart Display | Main MCU + Touch LCD |
| AD8232 | ECG Front End |
| PCM5102A | I2S Audio DAC |
| LiPo Battery | Portable Power |
| TP4056 | Battery Charging |
| Headphone Jack | Audio Output |
| Pocket Operator Jack | Sync Output |
| USB-C | Charging & Programming |

---

# GPIO Assignment

## ECG

| Module | ESP32 |
|----------|--------|
| AD8232 OUT | GPIO4 |
| LO+ | GPIO16 |
| LO- | GPIO17 |

---

## Display

Integrated ESP32 Smart Display

---

## Audio

| PCM5102 | ESP32 |
|-----------|--------|
| BCK | GPIO10 |
| LCK | GPIO11 |
| DIN | GPIO12 |

---

## Sync Output

| Function | ESP32 |
|-----------|--------|
| Pocket Operator Sync | GPIO13 |

---

# Software Stack

ESP-IDF

Arduino Framework

LVGL

I2S Audio

FreeRTOS

Bluetooth

WiFi

LittleFS

---

# User Interface

```
+----------------------------------------+
| BPM 72       BATTERY 88%               |
|                                        |
| ECG Waveform                           |
|                                        |
| ▄▁▂▃▄▅▆▇█                              |
|                                        |
| Piano Keyboard                         |
|                                        |
| ▮ ▮  ▮ ▮ ▮                             |
| ▯▯▯▯▯▯▯▯▯▯▯▯                           |
|                                        |
| [Chord] [Raw] [Record] [Settings]      |
+----------------------------------------+
```

---

# Audio Modes

## Raw ECG

Listen to amplified ECG waveform.

---

## Zen Mode

Heartbeat controls ambient sound.

---

## Piano Mode

Touch piano keyboard.

---

## Chord Mode

HiChord-inspired automatic chords.

---

## Sync Mode

Heartbeat drives Pocket Operator clock.

---

# PCB

Main sections:

```
Power

↓

ECG

↓

ESP32

↓

Audio

↓

Headphones

↓

Sync Output
```

---

# Enclosure

ABS Plastic

USB-C

Touch LCD

3.5 mm Headphones

3.5 mm Sync

ECG Connector

---

# Power

3.7V LiPo Battery

↓

TP4056 Charger

↓

3.3V Regulator

↓

ESP32 + Audio + ECG

---

# Safety

This project is:

✔ Creative

✔ Educational

✔ Music

This project is **NOT**

❌ Medical Equipment

❌ ECG Monitor

❌ Diagnostic Device

---

# Future Improvements

- MIDI USB
- BLE MIDI
- SD Card Recording
- Stereo Effects
- Looper
- Delay
- Reverb
- AI Chord Generator
- Cloud Sync
- OTA Firmware Updates

---

# Manufacturing

Prototype:

- 2 Units

Production:

- PCB Assembly
- 3D Printed Enclosure

Future:

- Injection Molded Case

---

# Repository Structure

```
ZenSync/

├── Hardware/
│   ├── PCB/
│   ├── Schematic/
│   ├── Gerber/
│   ├── BOM/
│   └── Enclosure/
│
├── Firmware/
│   ├── ECG/
│   ├── Audio/
│   ├── LVGL/
│   ├── Bluetooth/
│   ├── WiFi/
│   └── Sync/
│
├── Documentation/
│
├── Images/
│
└── README.md
```

---

# License

MIT License

---

# Author

**Mwamuzi Shadrick**

Project:

**Zen Sync**

*"Where heartbeat becomes music."*
````

This README aligns with the project requirements checklist by documenting the product overview, hardware architecture, component list, GPIO mapping, firmware structure, PCB overview, enclosure, manufacturing plan, and safety statement, making it suitable for both GitHub and sharing with a PCB/PCBA manufacturer. 
