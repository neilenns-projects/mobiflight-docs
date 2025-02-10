---
title: Configuring inputs
description: Step-by-step guide for configuring MIDI devices as an input in MobiFlight.
weight: 20
---

## Key, button and pad inputs

These inputs are configured in MobiFlight using [the button and switch configuration process](/devices/button-switch/configuring-input).

When selecting the **Module** and **Device**, select the appropriate MIDI device and key. Alternatively, press the **Scan for input** button and press the key to automatically detect and select the input.

{{< screenshot image="input-selected-key.png" title="Screenshot of the input configuration dialog with a MIDI device and key selected." >}}

## Knob, slider and joystick inputs

These inputs are configured in MobiFlight using [the potentiometer configuration process](/devices/potentiometer/configuring-input).

When selecting the **Module** and **Device**, select the appropriate MIDI device and knob. Alternatively, press the **Scan for input** button and move the knob to automatically detect and select the input.

{{< screenshot image="input-selected-knob.png" title="Screenshot of the input configuration dialog with a MIDI device and knob selected." >}}

> [!TIP]
> Preset that take analog values are typically designed for a potentiometer with a range of 0-–1023. Knobs and other analog MIDI inputs provide values from 0--127.
>
> Use the [HubHop potentiometer tool](https://hubhop.mobiflight.com/tools/) to generate the correct event code to map the range to the expected values for the input.
