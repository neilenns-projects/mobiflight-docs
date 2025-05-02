---
title: ESP32 Boards
description: Details on MobiFlight incompatibility with ESP32 boards.
ogimage: card-images/boards/arduino-nano-esp32.png
---

> [!IMPORTANT]
> These boards are unsupported. Consider a [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico) instead.

While various boards with ESP32 chips are available as a pin-compatible replacement for other
microcontroller boards, the different architecture of the ESP32 processor requires a firmware
designed for the ESP32 platform. Since MobiFlight does not include an ESP32-compatible firmware,
boards using ESP32 chips are not supported.

{{< cards >}}

{{< card title="Arduino Nano ESP32" subtitle="ESP32-S3 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-esp32.png" >}}

{{</ cards >}}
