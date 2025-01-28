---
title: Arduino Nano
description: Details on MobiFlight support for the Arduino Nano.
ogimage: card-images/boards/nano.png
weight: 20
---

{{< buy-in-shop url="https://shop.mobiflight.com/product/arduino-nano-usb-c" >}}

The Arduino Nano is a compact board that trades a smaller size for fewer IO pins than the Arduino Mega boards. It is a great choice when space is at a premium.

{{< cards >}}

{{< card title="Arduino Nano" subtitle="ATmega328P microcontroller" image="card-images/boards/nano.png" >}}

{{</ cards >}}

> [!WARNING]
> Many lower-cost Nano boards, particularly those purchased from AliExpress, use the CH340G chip for serial communication to the PC. These chips are frequently counterfeit and require [additional driver installation](/guides/installing-drivers/).
>
> Purchasing an Arduino Nano [from the MobiFlight Shop](https://shop.mobiflight.com/product/arduino-nano-usb-c) ensures you will get a board with genuine chips.

## Specifications

- 14 digital IO pins, 6 with PWM support.
- 8 analog inputs (can be used as digital inputs).

## Pinout

{{< pinout >}}

> [!NOTE]
> Pins D0 and D1 are not available for use, as they are reserved for USB serial communication.
>
> Pins A6 and A7 are only available for analog input, they cannot be used as digital inputs.

## Additional resources

- [Buy from the MobiFlight shop and help support the project](https://shop.mobiflight.com/product/arduino-nano-usb-c)
- [3D model](https://grabcad.com/library/arduino-nano-ch430g-1)
- [Official technical documentation](https://docs.arduino.cc/hardware/nano/)
- [Pinout diagram (PDF)](pinout.pdf)
