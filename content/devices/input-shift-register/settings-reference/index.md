---
title: Settings reference
description: Description of all available settings for input shift register devices and input configurations using shift registers.
ogimage: card-images/devices/input-shift-register.png
weight: 40
---

## Modules dialog

{{< screenshot image="input-shift-register-configuration.png" title="Screenshot of the Modules dialog with the input shift register configuration showing." >}}

| Setting              | Description                                                                                                                                                    |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Latch                | The board pin connected to the latch input on the shift register. All digital and analog pins are supported.                                                   |
| Clock                | The board pin connected to the clock input on the shift register. All digital and analog pins are supported.                                                   |
| Data                 | The board pin connected to the data input on the shift register. All digital and analog pins are supported.                                                    |
| # of 8 bit registers | The number of 8-bit groups connected in series to the board. Chips with eight inputs count as one group. Chips with 16 inputs count as two groups.             |
| Name                 | The name for the input shift register. Displayed in the input configuration dialog to identify the shift register when mapping the input to a simulator event. |

## Input configuration

Input shift registers have the same input setting events as [buttons and switches](/devices/button-switch/settings-reference/#input-configuration).

Use the **Device** dropdowns to select the input shift register and specific input on the chain of shift registers to use.

{{< screenshot image="input-configuration.png" title="Screenshot of the input configuration wizard for an input shift register, with the InputShifter register and input 0 selected." >}}
