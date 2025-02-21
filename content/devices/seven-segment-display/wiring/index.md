---
title: Wiring
description: Step-by-step instructions for wiring a seven segment display module.
ogimage: card-images/devices/seven-segment-display-max7219.png
weight: 10
prev: /devices/seven-segment-display/
---

{{< tabs items="MAX7219 modules,TM1637 modules" >}}

{{< tab >}}

The **DIN**, **CS**, and **CLK** pins can be connected to any digital or analog input pin on the board.

{{< schematic image="max7219.svg" download="max7219.pdf" title="Schematic for wiring up to eight MAX7219 display modules in series." >}}

> [!WARNING]
> MAX7219 modules are sensitive to poor electrical connections and low voltage.
>
> Always use high-quality cables and an external +5V power source when connecting these modules to a board. When chaining multiple MAX7219 modules do not daisy-chain the +5V power.

{{< /tab >}}

{{< tab >}}

The **DIO** and **CLK** pins can be connected to any digital or analog input pin on the board. TM1637 modules cannot be connected in series.

{{< schematic image="tm1637.svg" download="tm1637.pdf" title="Schematic for wiring a TM1637 display module." >}}

{{< /tab >}}

{{< /tabs >}}
