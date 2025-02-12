---
title: Settings reference
description: Description of all available settings for output shift register devices and output configurations using shift registers.
ogimage: card-images/devices/output-shift-register.png
weight: 40
---

## Modules dialog

{{< screenshot image="output-shift-register-configuration.png" title="Screenshot of the Modules dialog with the output shift register configuration showing." >}}

| Setting              | Description                                                                                                                                                          |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Latch                | The board pin connected to the latch input of the shift register. All digital and analog pins are supported.                                                         |
| Clock                | The board pin connected to the clock input of the shift register. All digital and analog pins are supported.                                                         |
| Data                 | The board pin connected to the data output of the shift register. All digital and analog pins are supported.                                                         |
| # of 8 bit registers | The number of 8-bit groups connected in series to the board. Chips with eight inputs count as one group. Chips with 16 inputs count as two groups.                   |
| Name                 | The name for the output shift register. Displayed in the output configuration dialog to identify the shift register when mapping a simulator variable to the output. |

## Output display configuration

{{< tabs items="Single output,Multiple outputs" >}}

{{< tab >}}

{{< screenshot image="single-output.png" title="Screenshot of the Display tab with the ShiftRegister output type selected for a single output." >}}

{{< /tab >}}

{{< tab >}}

{{< screenshot image="multiple-outputs.png" title="Screenshot of the Display tab with the ShiftRegister output type selected for multiple outputs." >}}

{{< /tab >}}
{{< /tabs >}}

| Setting         | Description                                                                           |
| --------------- | ------------------------------------------------------------------------------------- |
| Shift Register  | The chain of shift registers to display the value on.                                 |
| Select Pins     | The output on the shift register chain to display the value on.                       |
| Select multiple | When checked, enables selecting multiple shift register outputs to display the value. |
