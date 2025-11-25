---
title: Servos
description: How to use servos with MobiFlight.
ogimage: card-images/devices/servo.png
next: /devices/servo/wiring/
---

Servos are a popular device in RC models and are useful for displaying values with a needle or indicator in cockpit builds.

{{< cards >}}
{{< card title="Servos" image="card-images/devices/servo.png" >}}
{{< /cards >}}

For information on how many servos can be connected to a board, see the [boards](/boards/) documentation.

## Popular options

The most widely used servo with MobiFlight is often referred to as a "[9g micro servo](https://www.amazon.com/s?k=micro+servo+motor)" and is sold in multipacks.

> [!WARNING]
> Some servos are described as `360 degree servos`. These servos have a mid-point position when provided a value of 512, move left when provided a value less than 512, and move right when provided a value greater than 512. Since they rotate continuously when given a value, they are not suitable for making gauges like altitude indicators.
>
> For gauges that need full 360 degree rotation use a [stepper motor](/devices/stepper-motor) instead.
