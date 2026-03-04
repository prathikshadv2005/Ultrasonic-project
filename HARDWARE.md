# 🔌 Circuit Wiring

## 📍 Connections

| HC-SR04 Pin | Raspberry Pi 4 Pin |             GPIO             |
|-------------|--------------------|------------------------------|
| VCC         | Pin 2              | 5V                           |
| GND         | Pin 6              | GND                          |
| TRIG        | Pin 16             | GPIO23                       |
| ECHO        | Pin 18             | GPIO24 (via voltage divider) |

---

## ⚠️ Voltage Divider for ECHO

The ECHO pin outputs 5V, but Raspberry Pi GPIO works at 3.3V.

Use:
- 1kΩ resistor between ECHO and GPIO24
- 2kΩ resistor between GPIO24 and GND

This reduces 5V to ~3.3V and protects the Raspberry Pi.

---

## 📷 Circuit Diagram

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/74a543f1-081b-404c-80f8-d81f4405968e" />
