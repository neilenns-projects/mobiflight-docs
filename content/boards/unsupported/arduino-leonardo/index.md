---
title: Arduino Leonardo
description: Details on MobiFlight incompatibility with the Arduino Leonardo.
ogimage: card-images/boards/arduino-leonardo.png
---

> [!IMPORTANT]
> This board is unsupported. Consider a [Mega 2560 Pro Mini](/boards/recommended/mega-2560-pro-mini/) instead.

The Arduino Leonardo is an Arduino board based on the ATmega32U4 microcontroller.
Despite its physical resemblance to the Arduino Uno, it is more closely related to the [Arduino Micro](/boards/unsupported/arduino-micro),
another unsupported board.

{{< cards >}}

{{< card title="Arduino Leonardo" subtitle="ATmega32U4 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-leonardo.png" >}}

{{</ cards >}}

While it is sometimes possible to install MobiFlight Pro Micro firmware on the Arduino Leonardo,
this should not be taken as a sign of support. The MobiFlight Pro Micro firmware was not designed
or tested with the Arduino Leonardo in mind, so attempting to use it on the Leonardo board may
lead to issues, including but not limited to missing pins.
