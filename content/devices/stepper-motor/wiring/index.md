---
title: Wiring
description: Step-by-step instructions for wiring stepper motors.
ogimage: card-images/devices/stepper-motor.png
weight: 10
prev: /devices/stepper-motor/
---

{{< tabs items="28BYJ-48 with ULN2003 driver,Nema 17 with TB6600 driver">}}

{{< tab >}}
The **IN1**, **IN2**, **IN3** and **IN4** pins can be connected to any digital or analog input pin on the board.

{{< schematic image="uln2003.svg" download="uln2003.pdf" title="Schematic for wiring a ULN2003 driver." >}}

{{< /tab >}}

{{< tab >}}

The **PUL- (PUL)** and **DIR- (DIR)** pins can be connected to any digital or analog input pin on the board.

Connecting **ENA-(EN)** is optional and only required when the stepper should be enabled by a specific simulator output (for example, auto-throttle or autopilot engaged).

{{< schematic image="tb6600.svg" download="tb6600.pdf" title="Schematic for wiring a TB6600 driver." >}}

{{< /tab >}}

{{< /tabs>}}
