---
title: Wiring
description: Step-by-step guide for wiring LCDs.
ogimage: card-images/devices/lcd-20x4.png
weight: 10
prev: /devices/lcd/
---

<!-- Two separate GitHub info bocks in a row cause this markdownlint error. >
<!-- markdownlint-disable MD028 -->

{{< schematic image="schematic.svg" download="schematic.pdf" title="Schematic for wiring an LCD." >}}

> [!WARNING]
> LCDs must be connected to an external +5V power source. Do not use the +5V pin on a [board](/boards/) for power.

> [!IMPORTANT]
> LCDs can only be connected to specific pins on a board, typically labeled **SDA** and **SCL**. Check the pinout diagram on the [boards](/boards/) page and verify the LCD is connected to the appropriate pins.
