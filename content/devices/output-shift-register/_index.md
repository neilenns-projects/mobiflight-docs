---
title: Output shift registers
description: How to use output shift registers with MobiFlight.
ogimage: card-images/devices/output-shift-register-dm13a.png
next: /devices/output-shift-register/wiring
---

LEDs are the most common output device when building panels, and it is often the case where the number of LEDs exceed the number of output pins or current available on a board. Output shift registers, in particular LED driver chips, solve this issue. They provide individual control of many LEDs using only three pins on a board. The brightness of all connected LEDs can be controlled by using a fourth board pin.

{{< cards >}}
{{< card title="74HC595" subtitle="Basic output shift register" image="card-images/devices/output-shift-register-74hc595.png" >}}
{{< card title="DM13A" subtitle="LED driver for 16 LEDs" image="card-images/devices/output-shift-register-dm13a.png" >}}
{{< /cards >}}

For information on how many output shift registers can be connected to a board, see the [boards](/boards/) documentation.

## Popular options

There are several output shift registers commonly used in panel builds. One is a basic shift register, the rest are specifically designed to manage multiple LEDs.

| Chip    | Use                         |
| ------- | --------------------------- |
| 74HC595 | Basic output shift register |
| DM13A   | LED driver for 16 LEDs      |
| TLC5917 | LED driver for 8 LEDs       |

> [!TIP]
> When using a shift register to drive LED output, it is best to use a dedicated LED driver chip instead of the basic
> 74HC595 output shift register.

## Other options

There are many chips that function as an output shift register, including many designed for LED output. The following are usually pin compatible with the [popular options](#popular-options), but check the specific chip's data sheet to confirm.

- DM134/5/6
- DM13A
- FD9802
- MBI5024
- MBI5026
- MBI5041
- SCT2026
- SCT2210
- STP16CP05
- TB62701
- TB62706
- TB62709
- TB62747
- TC62D748
- TLC5927
- TLC5928
- TLC59283
- TLC5940

## Additional resources

- [74HC595 datasheet](https://www.ti.com/lit/gpn/sn74hc595)
- [DM13A datasheet](https://www.alldatasheet.com/datasheet-pdf/pdf/307093/SITI/DM13A.html)
- [TLC5917 datasheet](https://www.ti.com/lit/gpn/tlc5917)
