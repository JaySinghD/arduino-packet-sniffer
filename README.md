# ESP32 Arduino Packet Sniffer

This project is a basic network packet sniffer built using an ESP32 microcontroller. It captures wireless traffic over Wi-Fi using the ESP32's built-in promiscuous mode and parses selected packet headers. It's designed as a learning tool for understanding low-level network protocols and basic intrusion detection techniques like ARP spoofing detection.

## Overview

The ESP32 monitors nearby Wi-Fi traffic and extracts information such as MAC addresses, protocol types, and packet types. The system can optionally filter and flag suspicious activity, such as ARP spoofing.

## Features

- Promiscuous mode packet capture using ESP32
- Header parsing for 802.11 Wi-Fi frames
- Identification of basic packet types (e.g. ARP, IP)
- ARP spoofing detection logic

## Hardware Requirements

- ESP32 development board (ESP32-S3 Model)
- USB-C cable
- Breadboard, jumper wires, LED, and resistors

## Software Requirements

- Arduino IDE with ESP32 board support installed
- Serial monitor (built into Arduino IDE)
- `esp32-sniffer.ino` sketch (in this repository)

## Setup

1. Clone or download this repository.
2. Open `esp32-sniffer.ino` in the Arduino IDE.
3. Connect the ESP32 via USB and select the correct board and port.
4. Upload the sketch to the device.
5. Open the Serial Monitor at 115200 baud to view live packet data.

## Use Case: ARP Spoofing Detection

One simple application of this project is detecting ARP spoofing attempts. The sketch monitors ARP replies and checks if the same IP is being claimed by multiple MAC addresses. If this pattern is detected, it prints a warning to the serial monitor.

## Limitations

- ESP32 cannot decrypt encrypted Wi-Fi payloads (only headers are accessible).
- Packet capture is limited to the current Wi-Fi channel.
- Not suitable for high-throughput or enterprise-level packet inspection.
- Only 2.4 GHz Wi-Fi is supported (not 5 GHz).

## Project Goals

To learn about:
- Network debugging
- Intrusion detection
- Protocol analysis
- How network communication actually works


## Development Log

| Date       | Milestone                                      |
|------------|------------------------------------------------|
| June 16    | Researched hardware and software requirements |
| June 17    | Purchased and aranged required hardware |
| June 18    | Initial setup for ESP32-S3 microcontroller and Arduino IDE. Learning how to use ESP32-S3 |
| June 22| Learning how to use ESP32-S3 |
| June 23| Encountered issue with ESP32-S3. Contacted manufacturer support. |
| June 25| Resolved issue. Learned about ESP32-S3 capabilities related to Wi-Fi:|
