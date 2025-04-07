---
title: Turning 7-Segment displays on and off
description: How to turn 7-segment displays on and off using an output configuration.
---

7-segment displays can have their brightness set using the value of an output configuration. This is most often used to turn the displays off and on based on whether the avionics have power.

The following steps demonstrate how to use an airplane's avionics power state in a Cessna 172 to turn a MAX7219 display module off and on in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!NOTE]
> This guide assumes an [output configuration](/devices/seven-segment-display/configuring-output/) is already created to display a value on the display.

{{% steps %}}

### Create an output configuration for the brightness

Add an output configuration named **Display brightness**. Select the **CIRCUIT GENERAL PANEL ON** preset.

This preset is `0` when the avionics do not have power and `1` when they do.

{{< screenshot image="display-brightness-output-config.png" title="Screenshot of an output configuration with the CIRCUIT GENERAL PANEL ON preset highlighted." >}}

### Add a transform modifier to battery output

On the **Modify** tab for the output created in the previous step, add a [**Transform** modifier](/features/modifiers/transform/) and set the value to `$*5`. This multiplies the value from the simulator (either `0` or `1`) by five to provide a brightness value of `5` when the avionics have power.

{{< screenshot image="display-brightness-modify.png" title="Screenshot of an output configuration with the Modify tab selected and a transform modifier added." >}}

> [!TIP]
> 7-segment displays support 1--15 for brightness values. Adjust the brightness of the display when on by changing `5` to the desired brightness level.
>
> To get a dynamic brightness level, add a config reference on the **Modify** tab to an output configuration that returns a value of 1--15, and use it in place of the fixed `5` value.

### Use the avionics power output to control the brightness

On the **Display** tab for the 7-segment display output configuration, set the **Brightness ref.** dropdown to the output configuration added in the first step.

{{< screenshot image="brightness-ref.png" title="Screenshot of the 7-segment display output configuration with the Display tab selected, and the Brightness ref dropdown set to Display brightness." >}}

{{% /steps %}}
