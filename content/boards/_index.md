---
title: Boards
description: Details on supported boards and how to connect to MobiFlight
ogimage: card-images/boards/mega-2560-pro-mini.png
toc: false
breadcrumbs: false
weight: 20
cascade:
  type: docs
---

MobiFlight supports a wide range of different boards as the foundation for connecting [devices](/devices/).

> [!WARNING]
> Many boards have similar sounding names. Only the ones listed below are supported. See the
> [unsupported boards](/boards/unsupported) section for a list of boards that are often purchased by accident
> that will **not** work with MobiFlight.

## Recommended boards

{{< buy-in-shop url="https://shop.mobiflight.com/category/boards" >}}

These boards are all widely available, inexpensive, and are popular with MobiFlight users.

{{< cards >}}
{{< card link="recommended/mega-2560-pro-mini" title="Mega 2560 Pro Mini" subtitle="ATmega2560 microcontroller" image="card-images/boards/mega-2560-pro-mini.png" >}}
{{< card link="recommended/arduino-nano" title="Arduino Nano" subtitle="ATmega328P microcontroller" image="card-images/boards/nano.png" >}}
{{< card link="recommended/pro-micro" title="Pro Micro (16MHz)" subtitle="ATmega32U4 microcontroller" image="card-images/boards/pro-micro.png" >}}
{{< card link="recommended/raspberry-pi-pico" title="Raspberry Pi Pico 1" subtitle="RP2040 microcontroller" image="card-images/boards/raspberry-pi-pico.png" >}}
{{< /cards >}}

## Other supported boards

These boards are supported, but are older designs. If you already own one, they work fine. If you are
purchasing a new board, buy a [recommended board](/boards/recommended) instead.

{{< cards >}}
{{< card link="supported/arduino-mega-2560" title="Arduino Mega 2560 Rev3" subtitle="ATmega2560 microcontroller" image="card-images/boards/mega-2560-rev3.png" >}}
{{< card link="supported/arduino-uno" title="Arduino Uno R3" subtitle="ATmega328P microcontroller" image="card-images/boards/arduino-uno.png" >}}
{{< /cards >}}

## Unsupported boards

Many boards have similar names to MobiFlight supported boards, but differ enough to not be supported
by MobiFlight firmware. These boards may have various compatibility issues and should not be used
in MobiFlight setups. Use a [recommended board](/boards/recommended) instead.

{{< cards >}}

{{< card link="unsupported/esp32" title="Any ESP32 board" subtitle="ESP32 microcontroller family" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-esp32.png" >}}
{{< card link="unsupported/arduino-leonardo" title="Arduino Leonardo" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-leonardo.png" >}}
{{< card link="unsupported/arduino-micro" title="Arduino Micro" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-micro.png" >}}
{{< card link="unsupported/arduino-nano-ble" title="Arduino Nano 33 BLE" subtitle="nRF52840 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-ble.png" >}}
{{< card link="unsupported/arduino-nano-iot" title="Arduino Nano 33 IoT" subtitle="ATSAMD21 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-iot.png" >}}
{{< card link="unsupported/arduino-nano-esp32" title="Arduino Nano ESP32" subtitle="ESP32-S3 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-esp32.png" >}}
{{< card link="unsupported/arduino-nano-every" title="Arduino Nano Every" subtitle="ATMega4809 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-nano-every.png" >}}
{{< card link="unsupported/arduino-uno-r4" title="Arduino Uno R4" subtitle="Renesas RA4M1 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-uno-r4-minima.png" >}}
{{< card link="unsupported/pro-micro-8mhz" title="Pro Micro (8 MHz)" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/pro-micro-8.png" >}}
{{< card link="unsupported/raspberry-pi-pico-2" title="Raspberry Pi Pico 2" subtitle="RP2350 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/raspberry-pi-pico2.png" >}}

{{</ cards >}}
