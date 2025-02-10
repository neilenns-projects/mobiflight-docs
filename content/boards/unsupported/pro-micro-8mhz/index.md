---
title: Pro Micro (8 MHz)
description: Details on MobiFlight incompatibility with the Pro Micro clocked at 8 Mhz.
ogimage: card-images/boards/pro-micro-8.png
---

> [!IMPORTANT]
> This board is unsupported. Consider a [Pro Micro (16 MHz)](/boards/recommended/pro-micro) instead.

Some models of [Pro Micro](/boards/recommended/pro-micro) are offered at a reduced clock speed of 8 MHz.
MobiFlight is designed for use with the 16 MHz version of the board. Particularly on low-cost
AliExpress listings, it is important to pay close attention to the product description to avoid
buying the 8 MHz version instead. Pro Micro boards sold on the [MobiFlight Shop](https://shop.mobiflight.com/product/arduino-pro-micro-usb-c)
are always the 16 MHz version.

{{< cards >}}

{{< card title="Pro Micro (8 MHz)" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/pro-micro-8.png" >}}

{{</ cards >}}

While it is sometimes possible to install MobiFlight Pro Micro firmware on the slower model of Pro
Micro, this should not be taken as a sign of support. The MobiFlight Pro Micro firmware was not
designed or tested with the 8 MHz model in mind, so attempting to use it on the slower board
may lead to issues, including but not limited to failed communication between the board and
the computer.
