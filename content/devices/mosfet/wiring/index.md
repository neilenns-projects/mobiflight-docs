---
title: Wiring
description: Step-by-step guide to wiring MOSFETs to control an LED light strip.
ogimage: card-images/devices/mosfet.png
weight: 10
prev: /devices/mosfet/
---

The following schematic illustrates how to connect an IRF520 breakout board to a [12V LED light strip](https://www.amazon.com/gp/product/B0DFWCD97Z).

To support dimming, ensure the **SIG** pin is connected to a PWM-capable input on the board. The [boards](/boards/) page provides pinout diagrams for each board, indicating the pins that support PWM.

{{< schematic image="schematic.svg" title="Schematic for wiring a MOSFET breakout board and LED light strip to a board." >}}

> [!IMPORTANT]
> The GND from the +12V power supply and the GND pin of the board must be connected.
