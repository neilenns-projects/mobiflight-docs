---
title: Wiring
description: Step-by-step instructions for wiring potentiometers.
weight: 10
prev: /devices/potentiometer/
---

Potentiometers have three pins. The outer two pins are connected to +5V and GND respectively. The middle pin is connected to an analog input on the board.

> [!WARNING]
> On 3.3V microcontroller boards such as the [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico/), connect the +5V end to +3.3V instead to be able to use the full range of the potentiometer and to minimize the risk of damage to the microcontroller.

{{< schematic image="potentiometer.svg" download="potentiometer.pdf" title="Schematic for wiring a potentiometer." >}}

> [!TIP]
> See the [boards page](/boards/) for pinout diagrams with the available analog pins on each supported board.
