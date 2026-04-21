# ESP32-H2 BLE Tag Standalone Project

## Project overview

This repository contains a standalone embedded project for building a BLE tag on the **ESP32-H2-DevKitM-1** using **Espressif ESP-IDF**.

The project is focused on learning how to build the **tag side** of a BLE-based system. The tag should advertise, be discoverable and connectable, receive a payload through a writable BLE characteristic, send an acknowledgment after the payload is received, and display the relevant payload fields on a **2.13" e-paper module by WeAct Studio**.

At the current stage, **nRF Connect** is used as the test client to discover the tag, connect to it, and write payload data.

---

## Purpose

The purpose of this repository is to learn and implement the core parts of a BLE tag on ESP32-H2, including:

- BLE advertising
- BLE discoverability and connectivity
- GATT service and characteristic design
- Receiving data from a BLE client
- Sending acknowledgment back to the client
- Filtering the received payload so only required fields are used
- Displaying the required fields on the e-paper display

This is a standalone learning project focused on understanding the BLE tag behavior step by step.

---

## Scope

### In scope

This repository currently focuses on:

- ESP32-H2 firmware for the BLE tag
- BLE advertising and connection handling
- GATT services and characteristics
- Receiving a payload from a BLE client
- Sending an acknowledgment after payload reception
- Filtering payload fields for display
- E-paper display integration
- Testing with nRF Connect

### Out of scope

This repository does not currently cover:

- Gateway implementation
- Backend implementation
- Cloud services
- Mobile application development beyond using nRF Connect for testing
- Full end-to-end production system design

---

## Current project goal

The intended tag behavior in this repository is:

1. The ESP32-H2 advertises as a BLE peripheral
2. The tag is discoverable and connectable
3. A client writes a payload to the tag
4. The tag receives the payload
5. The tag sends an acknowledgment back
6. The tag extracts only the fields needed for display
7. The selected data is shown on the e-paper display

For now, **nRF Connect** acts as the BLE client during testing.

---

## Main hardware

The main hardware used in this project is:

- **ESP32-H2-DevKitM-1**
- **USB cable** with at least **USB-C on the ESP32 side**
- **2.13" e-paper module by WeAct Studio**
- **A phone with the nRF Connect app** installed

---

## Main software

The main software and tools used in this project are:

- **Espressif ESP-IDF**
- **C / C++** for firmware development
- **nRF Connect** for BLE testing
- **Serial monitor** for debugging
- **GitHub** for repository and issue tracking

---

## Current repository structure

The repository currently contains:

- [`CMakeLists.txt`](./CMakeLists.txt) - top-level ESP-IDF project configuration
- [`main/CMakeLists.txt`](./main/CMakeLists.txt) - component build configuration for the main application
- [`main/main.c`](./main/main.c) - current application entry point and main firmware source file

---

## Documentation

This root README is intended to describe the repository purpose and scope.

Additional documentation, such as setup, build, flash, and hardware notes, will be added later as separate files when those documents are created in the repository.

---

## Notes

This repository is specifically about the **BLE tag** side of the project.

The README should continue to reflect the actual scope of the repository and should be updated as the project evolves so it does not claim features that are not yet implemented.