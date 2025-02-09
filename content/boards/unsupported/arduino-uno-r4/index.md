---
title: Arduino Uno R4
description: Details on MobiFlight incompatibility with the Arduino Uno R4.
ogimage: card-images/boards/arduino-uno-r4-minima.png
---

> [!IMPORTANT]
> This board is unsupported. Consider a [Mega 2560 Pro Mini](/boards/recommended/mega-2560-pro-mini/) instead.

The Arduino Uno R4 is an Arduino board based on the Renesas RA4M1 microcontroller.
While it bears the Arduino Uno name and is prominently featured on the Arduino website as the
successor of the Arduino Uno R3, the fact that it uses a different microcontroller than the
latter makes it incompatible with MobiFlight firmware. Arduino's advertised sketch compatibility
applies only to Arduino sketches the user builds in the Arduino IDE, not pre-made firmware images
like MobiFlight.

{{< cards >}}

{{< card title="Arduino Uno R4 Minima" subtitle="Renesas RA4M1 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-uno-r4-minima.png" >}}
{{< card title="Arduino Uno R4 Wi-Fi" subtitle="Renesas RA4M1 microcontroller" tag="Unsupported" tagType="error" image="card-images/boards/arduino-uno-r4-wifi.png" >}}

{{</ cards >}}

The Arduino Uno R4 comes in two variants, Minima and WiFi. Both are incompatible with MobiFlight firmware.
