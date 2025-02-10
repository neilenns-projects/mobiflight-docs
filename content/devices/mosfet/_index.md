---
title: MOSFETs
description: How to use MOSFETs with MobiFlight.
ogimage: card-images/devices/mosfet.png
next: /devices/mosfet/wiring/
---

MOSFETs are a popular option for controlling backlights in a cockpit build. They are a convenient way to control [dimmable COB light strips](https://www.amazon.com/gp/product/B0DFWCD97Z) from a MobiFlight output.

{{< cards >}}
{{< card title="MOSFETs" subtitle="Breakout board for the IFR520 MOSFET" image="card-images/devices/mosfet.png" >}}
{{</ cards >}}

To use MOSFETs with MobiFlight, follow the [LED guide](/devices/leds/) to configure them as outputs.

## Popular options

[Breakout boards](https://www.amazon.com/HiLetgo-IRF520-MOSFET-Arduino-Raspberry/dp/B01I1J14MO) with the MOSFET installed and screw terminals for 12V power are a good starting option. These typically use the IFR520 MOSFET.

> [!TIP]
> Be careful of the operating voltage and current for the MOSFET. There is a wide range of options, not all of which are suitable for use with MobiFlight supported boards. The IFR520 breakout board, for example, should not be used with the 3.3V data signals of the [Raspberry Pi Pico 1](/boards/raspberry-pi-pico/).
