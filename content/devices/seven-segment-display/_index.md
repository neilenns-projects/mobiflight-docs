---
title: 7-segment display modules
description: How to use 7-segment LED displays using the MAX7219 or TM1637 driver with MobiFlight.
ogimage: card-images/devices/seven-segment-max7219.png
next: /devices/seven-segment-display/wiring/
---

7-segment display modules are typically used to show radio frequencies (COM and NAV), autopilot values (HDG and SPD), and other numerical values from the simulator.

Modules using the MAX7219 driver chip are the most popular. MobiFlight also supports displays using the TM1637 driver.

{{< cards >}}

{{< card title="4-digit module" subtitle="Using the TM1637 driver" image="card-images/devices/seven-segment-tm1637-four-digits.png" >}}

{{< card title="6-digit module" subtitle="Using the TM1637 driver" image="card-images/devices/seven-segment-tm1637-six-digits.png" >}}

{{< card title="8-digit module" subtitle="Using the MAX7219 driver" image="card-images/devices/seven-segment-max7219.png" >}}

{{< /cards >}}

For information on how many 7-segment displays can be connected to a board, see the [boards](/boards/) documentation.

> [!WARNING]
> Some 8-digit boards use the 74HC595 chip as the driver, particularly when ordered from AliExpress. These boards are not supported by MobiFlight. Pay close attention when ordering and only purchase boards that use the MAX7219 or TM1637 chip.

## Other options

While pre-made modules are the easiest way to use 7-segment displays, it is possible to wire separate displays to MAX7219 or TM1637 chips. This is a more advanced option, typically only used when making custom PCBs.

When purchasing 7-segment displays, make sure to select common cathode displays when using a MAX7219 driver chip. Use common anode displays when connecting to a TM1637 driver chip.
