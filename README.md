# nRF BLE UART Echo

This project is a modified version of the **nRF BLE-UART sample**, running in **BLE Peripheral (GATT Server) mode**.

It supports bidirectional ASCII data relay between a USB COM port and a BLE Central device using BLE UART.

## Project Environment

* **IDE:** SEGGER Embedded Studio (SES)
* **Platform:** Nordic nRF
* **BLE Role:** Peripheral (GATT Server)
* **Communication:** BLE UART and USB COM

## Communication Flow

```text
+---------+       +------------------+       +--------------+
| USB COM | <-->  | BLE Peripheral   | <-->  | BLE Central  |
|         |       | (UART Relay)     |       |              |
+---------+       +------------------+       +--------------+
```

The Peripheral acts as a relay between the USB COM interface and the BLE Central device.

## Features

* BLE Peripheral / GATT Server operation
* BLE UART communication
* USB COM data transmission and reception
* Bidirectional ASCII data relay
* Echo-based communication testing

## How It Works

* **USB to BLE:** ASCII data received through USB COM is forwarded to the BLE Central.
* **BLE to USB:** ASCII data received from the BLE Central is forwarded to USB COM.

This allows bidirectional communication between a PC and a BLE Central device through the nRF Peripheral.

## Build

1. Open the project in **SEGGER Embedded Studio (SES)**.
2. Select the appropriate nRF target configuration.
3. Build and flash the firmware to the target device.

## Purpose

This project provides a simple test environment for verifying BLE UART communication, USB COM data transfer, and bidirectional ASCII relay between BLE devices and a PC.
