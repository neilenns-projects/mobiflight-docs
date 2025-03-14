---
title: Wiring
description: Step-by-step guide for wiring LCDs.
ogimage: card-images/devices/lcd-20x4.png
weight: 10
prev: /devices/lcd/
---

{{< schematic image="schematic.svg" download="schematic.pdf" title="Schematic for wiring an LCD." >}}

> [!IMPORTANT]
> LCDs can only be connected to specific pins on a board, typically labeled **SDA** and **SCL**. Check the pinout diagram on the [boards](/boards/) page and verify the LCD is connected to the appropriate pins.
>
> The **SDA** and **SDL** signals must be +5V. If connected to a [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico/) board, make sure to use a level shifter.
