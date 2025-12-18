# 🎨 Color Aid Device (Dual-STM32 • Wireless • C)

An assistive embedded system that **detects real-world colors** using an **RGB sensor** and communicates the result to a second unit that outputs the **color name on an LCD** and provides **audio feedback via a speaker**.

Built with **two STM32 boards** communicating wirelessly using **point-to-point radio**, with firmware written in **C**.

---

## ✨ Features
- 🌈 **RGB color sensing** (captures color readings from an object)
- 📡 **Wireless point-to-point radio link** (sensor unit → output unit)
- 📟 **LCD display** shows the detected **color name**
- 🔊 **Speaker output** announces the color for accessibility
- 🧠 On-device **color classification** (lightweight, embedded-friendly)
- 🧩 Split architecture: sensing node + output node

---

## 🧠 System Architecture

### 1) Sensor Node (STM32 #1)
- Reads the **RGB sensor** (Using I2C)
- Applies basic filtering/normalization
- Classifies the reading into a **human-friendly color name**
- Transmits the result over **P2P radio**

### 2) Output Node (STM32 #2)
- Receives color packets via radio
- Displays the **color name** on the **LCD**
- Triggers the **speaker** (tone/voice prompt depending on implementation)

---

## 🛠️ Tech Stack
- **Firmware:** C (bare-metal / HAL/LL-style embedded C)
- **MCU platform:** STM32
- **Wireless:** Point-to-point radio communication
- **Peripherals:** RGB sensor + LCD + speaker

---

## 🧱 Hardware
- 2× **STM32 development boards**
- 1× **RGB color sensor**
- 1× **LCD display**
- 1× **Speaker**
- 2× **Xbee Radio modules** configured for point-to-point communication

---
