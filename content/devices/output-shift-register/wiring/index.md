---
title: Wiring
description: Step-by-step instructions for wiring LEDs to output shift registers and LED driver chips.
ogimage: card-images/devices/output-shift-register-dm13a.png
weight: 10
math: true
prev: /devices/output-shift-register/
---

<!-- markdownlint doesn't understand multiple github info blocks in a row.  -->
<!-- markdownlint-disable-file MD028 -->

The following components are required for an output shift register or LED driver:

- The output shift register or LED driver chip.
- LEDs.
- Assorted resistors.
- 0.1µF capacitors.

{{< tabs items="74HC595 DIP-16,DM13A DIP-24,TLC5917 DIP-16">}}

{{< tab >}}
Pay close attention to the orientation of the LEDs: the anode (long leg) should be connected to the chip and the cathode (short leg) should be connected to GND. This is the opposite of how LEDs are connected to LED driver chips. The 200Ω resistors are required on every output pin with an LED attached.

{{< schematic image="74hc595.svg" download="74hc595.pdf" title="Schematic for wiring a single 74HC595 chip." >}}

> [!TIP]
> Using a DM13A or other similar LED driver chip is a better choice than using the 74HC595 for driving LEDs.

> [!TIP]
> Connecting pin 13, {{% overline %}}OE{{% /overline %}}, to a PWM pin on a board enables brightness control of the LEDs as a group from MobiFlight.

> [!TIP]
> To daisy-chain 74HC595 chips, connect the `QH'` pin (9) from one chip to the `SER` pin (14) of the next chip. All other control signals, including `SRCLK` (11) and `RCLK` (12), must be shared across all chained shift registers.

{{< /tab >}}

{{< tab >}}
Pay close attention to the orientation of the LEDs: the anode (long leg) should be connected to +5V and the cathode (short leg) should be connected to the chip. This is the opposite of how LEDs are connected to a 74HC595.

{{< schematic image="dm13a.svg" download="dm13a.pdf" title="Schematic for wiring a single DM13A chip." >}}

The value of $R_{\text{ext}}$ determines the amount of current for the LEDs. A 5kΩ resistor results in approximately 12mA per LED, a good brightness level for most situations.

> [!TIP]
> Connecting pin 21, {{% overline %}}EN{{% /overline %}}, to a PWM pin on a board enables brightness control of the LEDs as a group from MobiFlight.

> [!TIP]
> To daisy-chain DM13A chips, connect the `DAO` pin (22) from one chip to the `DAI` pin (2) of the next chip. Use a dedicated resistor for the `REXT` pin on each chip. All other control signals, including `DCK` and `LAT`, must be shared between all chained shift registers.

{{< /tab >}}

{{< tab >}}
Pay close attention to the orientation of the LEDs: the anode (long leg) should be connected to +5V and the cathode (short leg) should be connected to the chip. This is the opposite of how LEDs are connected to a 74HC165.

{{< schematic image="tlc5917.svg" download="tlc5917.pdf" title="Schematic for wiring a single TLC5917 chip." >}}

The value of $R_{\text{ext}}$ determines the amount of current for the LEDs. A 1.6kΩ resistor results in approximately 12mA per LED, a good brightness level for most situations.

> [!TIP]
> Connecting pin 13, {{% overline %}}OE{{% /overline %}}(ED2), to a PWM pin on a board enables brightness control of the LEDs as a group from MobiFlight.

> [!TIP]
> To daisy-chain TLC5917 chips, connect the `SDO` pin (14) from one chip to the `SDI` pin (2) of the next chip. Use a dedicated resistor for the `R-EXT` pin on each chip. All other control signals, including `CLK` and `LE(ED1)`, must be shared between all chained shift registers.

{{< /tab >}}

{{< /tabs>}}
