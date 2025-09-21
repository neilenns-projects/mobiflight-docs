---
title: Wiring
description: Step-by-step instructions for wiring potentiometers.
ogimage: card-images/devices/potentiometer.png
weight: 10
prev: /devices/potentiometer/
---

Potentiometers have three pins. The outer two pins are connected to microcontroller's supply voltage (usually +5V, but sometimes +3.3V) and GND respectively. The middle pin is connected to an analog input on the board.

> [!WARNING]
> On 3.3V microcontroller boards such as the [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico/), connect the potentiometer pin that would normally go to +5V to +3.3V instead. This makes it possible to use the full range of the potentiometer and minimizes the risk of damage to the microcontroller.

{{< schematic image="potentiometer.svg" download="potentiometer.pdf" title="Schematic for wiring a potentiometer." >}}

> [!TIP]
> See the [boards page](/boards/) for pinout diagrams with the available analog pins on each supported board.
