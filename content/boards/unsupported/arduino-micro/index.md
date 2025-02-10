---
title: Arduino Micro
description: Details on MobiFlight incompatibility with the Arduino Micro.
ogimage: card-images/boards/arduino-micro.png
---

> [!IMPORTANT]
> This board is unsupported. Consider an [Arduino Nano](/boards/recommended/arduino-nano) or [Pro Micro (16 MHz)](/boards/recommended/pro-micro) instead.

The Arduino Micro is an Arduino board based on the ATmega32U4 microcontroller.
While very similar to the [Pro Micro 16 Mhz](/boards/recommended/pro-micro), it is a different board with different
features that cause incompatibilities.

{{< cards >}}

{{< card title="Arduino Micro" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-micro.png" >}}

{{</ cards >}}

While it is sometimes possible to install MobiFlight Pro Micro firmware on the Arduino Micro,
this should not be taken as a sign of support. The MobiFlight Pro Micro firmware was not designed
or tested with the Arduino Micro (non-pro) in mind, so attempting to use it on the Arduino Micro
board may lead to issues, including but not limited to missing pins.
