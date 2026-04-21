# ESP-IDF setup and build guide

## Overview

This document points to the official ESP-IDF installation guide and shows a simple example workflow for building and flashing this repository.

This project targets the **ESP32-H2** and uses **Espressif ESP-IDF**.

---

## Install ESP-IDF

Follow the official Espressif documentation for your operating system:

- [ESP32-H2 Getting Started](https://docs.espressif.com/projects/esp-idf/en/stable/esp32h2/get-started/index.html)
- [macOS installation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32h2/get-started/macos-setup.html)
- [Linux installation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32h2/get-started/linux-setup.html)
- [Windows installation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32h2/get-started/windows-setup.html)

Follow the official guide to install ESP-IDF, the required tools, and the command-line environment.

---

## nRF Connect

Install **nRF Connect** on your phone:

- **Android**: Google Play
- **iPhone (iOS)**: App Store

---

## Example workflow for this repository

After ESP-IDF is installed and your environment is ready, run commands like these from the repository root.

### 1. Activate the ESP-IDF environment

```bash
source /path/to/activate_idf.sh
idf.py set-target esp32h2
idf.py build
idf.py -p PORT flash monitor // Replace PORT with the serial port for your board.

Replace `PORT` with the serial port for your board.

Examples:

- macOS: `/dev/cu.usbserial-XXXX`
- Linux: `/dev/ttyUSB0`
- Windows: `COM5`

---

## BLE test flow

After flashing the firmware:

1. Open **nRF Connect**
2. Scan for the BLE tag
3. Connect to the device
4. Discover services and characteristics
5. Test the relevant characteristic
6. Observe the device behavior and serial logs