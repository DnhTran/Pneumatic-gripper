
# ⚙️ STM32 GPIO Control Project

A simple yet effective STM32F103-based project that demonstrates real-time **GPIO control** using buttons and outputs like **LEDs** and **pneumatic motors**. Built using **STM32 HAL** libraries in **STM32CubeIDE**.

---

## 🚀 Overview

This project showcases how to:

- Read digital inputs from push buttons
- Control LEDs and 3 pneumatic motors
- Debounce buttons via software
- Implement toggle logic for directional control

---

## 🧰 Hardware Setup

| Component      | Description                      |
|----------------|----------------------------------|
| Microcontroller | STM32F103VCT6                    |
| Inputs         | 4 push buttons (PE13, PE12, PE10, PE11) |
| Outputs        | 1 LED, 3 pneumatic motors         |
| IDE            | STM32CubeIDE                     |
| Libraries      | STM32F1 HAL                      |

---

## 🎮 Functionality

| Button (GPIO) | Action                          |
|---------------|----------------------------------|
| **P1** (PE13) | Toggle **LED D1** ON/OFF         |
| **P2** (PE12) | Activate **Motor M1** (Grip/Release) |
| **P3** (PE10) | Move **Motor M2** Up/Down        |
| **P4** (PE11) | Toggle **Motor M3** Left/Right   |

---

## 🔌 Output Pin Mapping

| Output       | GPIO Label |
|--------------|------------|
| LED D1       | D0         |
| Motor M1     | Y1         |
| Motor M2     | Y2         |
| Motor M3 Left| S4         |
| Motor M3 Right| S3        |

---

## 🧠 How It Works

Each button is polled inside the `main()` loop:

- 🟢 **P1**: LED turns ON when pressed, OFF when released.
- 🤖 **P2**: Gripper motor (M1) is activated while button is held.
- ⬆️ **P3**: Lifting motor (M2) moves UP while pressed, down when released.
- ↔️ **P4**: Toggles horizontal direction (Left ↔ Right) for M3 on each press.

---

## 📁 Project Structure

