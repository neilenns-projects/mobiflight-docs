---
title: Wiring
description: Step-by-step guide for wiring buttons and switches to input shift registers.
ogimage: card-images/devices/input-shift-register.png
weight: 10
prev: /devices/input-shift-register/
---

The following components are required to wire buttons to an input shift register:

- A 74HC165 chip.
- Buttons or switches.
- 10kΩ resistors.
- 0.1µF capacitors.

> [!IMPORTANT]
> MobiFlight only supports connecting buttons to input shift registers. Encoders must be connected directly to a board.

{{< tabs >}}

{{< tab name="Single 74HC165 DIP-16" >}}
The 10kΩ resistors are required on every input pin, even if you aren't attaching a button to that pin, to avoid false input events.

{{< schematic image="single-chip.svg" download="single-chip.pdf" title="Schematic for wiring a single 74HC165 chip." >}}

{{< /tab >}}

{{< tab name="Four 74HC165 DIP-16 in series" >}}
MobiFlight supports up to four 74HC165 chips connected in series. When wiring the chips it is important to wire them with the right most chip in the series one connected to the board's data input line. The clock and latch pins are shared across all chips.

{{< schematic image="multiple-chips.svg" download="multiple-chips.pdf" title="Schematic for wiring four 74HC165 chips in series." >}}

(Buttons and pull-up resistors omitted for clarity)

{{< /tab >}}

{{< /tabs >}}

> [!TIP]
> For 3.3V microcontrollers like the [Raspberry Pi Pico 1](/boards/recommended/raspberry-pi-pico/), the shift register should be powered from +3.3V instead of +5V unless a level shifter is used.
