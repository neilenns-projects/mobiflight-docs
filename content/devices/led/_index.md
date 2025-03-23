---
title: LEDs
description: How to use LEDs with MobiFlight.
ogimage: card-images/devices/led.png
next: /devices/led/wiring/
---

LEDs are the most common output device used with MobiFlight. They are used as indicators and backlighting, and are a core component of every build.

{{< cards >}}
{{< card title="LEDs" image="card-images/devices/led.png" >}}
{{</ cards >}}

For information on how many LEDs can be connected to a board, see the [boards](/boards/) documentation.

## Popular options

5mm LEDs are inexpensive, available in a wide range of colors, and are easy to work with. 3mm LEDs are smaller and a good choice when space is tight.

## Limitations

Boards are limited in the number of LEDs they can drive simultaneously due to current restrictions. Each board pin can typically supply or sink a maximum of 20-40 mA, and the total current draw for all pins combined must not exceed the board's rated limit, often around 200-400 mA. Exceeding these limits can cause the board to behave unpredictably.

To control more LEDs from a single board, consider using an LED driver chip, which can be connected to MobiFlight as an [output shift register](/devices/output-shift-register).
