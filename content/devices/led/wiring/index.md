---
title: Wiring
description: Step-by-step guide to wiring LEDs.
ogimage: card-images/devices/led.png
weight: 10
prev: /devices/led/
---

The following components are required to wire an LED:

- The LED
- A resistor, typically 220Ω

Connect the anode end of the LED (usually the longer leg) to the resistor, then connect the resistor to one of the digital pins of your board and the cathode end (usually the shorter leg) to GND.

{{< schematic image="led.svg" download="led.pdf" title="Diagram of wiring an LED with a 220Ω resistor to a board." >}}
