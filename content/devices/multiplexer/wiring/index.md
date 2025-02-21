---
title: Wiring
description: Step-by-step guide for wiring buttons and switches to multiplexers.
ogimage: card-images/devices/multiplexer.png
weight: 10
prev: /devices/multiplexer
---

The following components are required to wire a 74HC4067 breakout board:

- A 74HC4067 breakout board.
- Buttons or switches.

> [!IMPORTANT]
> MobiFlight only supports connecting buttons to multiplexers. Encoders must be connected directly to a board.

{{< schematic image="schematic.svg" download="schematic.svg" title="Schematic for wiring a 74HC4067 breakout board." >}}

The +5V power can come directly from the connected board. The 10kΩ resistor between DATA and +5V is optional, however it can help if there are issues with button presses being detected correctly.

When using the chip directly without a breakout board, ensure the {{% overline %}}EN{{% /overline %}} pin is connected to GND through a 10kΩ resistor.

> [!TIP]
> When connecting additional multiplexers to the same board, they can share the **S0--S3** pins. Each multiplexer must use a dedicated **Data** pin.
