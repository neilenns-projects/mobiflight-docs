---
title: Wiring
description: Step-by-step instructions for wiring potentiometers.
weight: 10
prev: /devices/potentiometer/
---

Potentiometers have three pins. The outer two pins are connected to +5V and GND respectively. The middle pin is connected to an analog input on the board.

> [!WARNING]
> Some boards, such as the [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico/), use 3.3V logic and have ADCs that only support 3.3V input. For these boards, connect the potentiometer to +3.3V instead of +5V to prevent damage to the board. Refer to your board's documentation for the correct voltage.
> [!TIP]
> See the [boards page](/boards/) for pinout diagrams with the available analog pins on each supported board.

{{< schematic image="potentiometer.svg" download="potentiometer.pdf" title="Schematic for wiring a potentiometer." >}}
