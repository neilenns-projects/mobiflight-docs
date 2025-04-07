---
title: Controlling 7-Segment display brightness
description: How to control 7-segment display brightness an output configuration.
---

<!-- Because steps are used in this document the headings across steps are duplicate. Disable the markdownlint -->
<!-- warning for those headings. -->
<!-- markdownlint-disable MD024 -->

7-segment displays can have their brightness set using the value of an output configuration. This is most often used to turn the displays off and on based on whether the avionics have power, or to adjust the brightness based on the aircraft's panel backlight level.

> [!NOTE]
> This guide assumes an [output configuration](/devices/seven-segment-display/configuring-output/) is already created to display a value on the display.

## Turning the display on and off

The following steps demonstrate how to use an airplane's avionics power state in a Cessna 172 (G1000) to turn a MAX7219 display module off and on with Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

{{% steps %}}

### Create an output configuration for the brightness

Add an output configuration named **Display brightness**. Select the **CIRCUIT GENERAL PANEL ON** preset.

This preset is `0` when the avionics do not have power and `1` when they do.

> [!TIP]
> The variable for avionics power may be different in other aircraft.

{{< screenshot image="display-brightness-output-config.png" title="Screenshot of an output configuration with the CIRCUIT GENERAL PANEL ON preset highlighted." >}}

### Add a transform modifier to avionics power output

On the **Modify** tab for the output created in the previous step, add a [**Transform** modifier](/features/modifiers/transform/) and set the value to `$*5`. This multiplies the value from the simulator (either `0` or `1`) by five to provide a brightness value of `5` when the avionics have power.

{{< screenshot image="display-brightness-modify.png" title="Screenshot of an output configuration with the Modify tab selected and a transform modifier added." >}}

> [!TIP]
> 7-segment displays support 1--15 for brightness values. Adjust the brightness of the display when on by changing `5` to the desired brightness level. See the [following section](/guides/seven-segment-brightness/#adjusting-the-brightness-display-based-on-the-panel-brightness) to use a dynamic brightness level.

### Use the avionics power output to control the display brightness

On the **Display** tab for the 7-segment display output configuration, set the **Brightness ref.** dropdown to the output configuration added in the first step.

{{< screenshot image="brightness-ref.png" title="Screenshot of the 7-segment display output configuration with the Display tab selected, and the Brightness ref dropdown set to Display brightness." >}}

{{% /steps %}}

## Adjusting the brightness display based on the avionics brightness

The following steps demonstrate how to use an airplane's avionics power state and avionics brightness value in a Cessna 172 (G1000) to control the brightness of a MAX7219 display with Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

{{% steps %}}

### Create an output configuration for the avionics power

Add an output configuration named **Avionics power**. Select the **CIRCUIT GENERAL PANEL ON** preset.

This preset is `0` when the avionics do not have power and `1` when they do.

{{< screenshot image="power-sim-variable.png" title="Screenshot of an output configuration with the CIRCUIT GENERAL PANEL ON preset highlighted." >}}

> [!TIP]
> The variable for avionics power may be different in other aircraft.

### Create an output configuration for the brightness

Add an output configuration named **Display brightness**. Select the **AVIONICS BRIGHTNESS** preset.

{{< screenshot image="brightness-sim-variable.png" title="Screenshot of an output configuration with the AVIONICS BRIGHTNESS preset highlighted." >}}

> [!TIP]
> The variable for avionics brightness may be different in other aircraft.

### Add a config reference for the avionics power

On the **Modify** tab for the **Display brightness** configuration, add a reference to the **Avionics power** output configuration.

{{< screenshot image="config-reference-avionics-power.png" title="Screenshot of an output configuration with a configuration reference added on the Modify tab." >}}

### Adjust the brightness value range

The brightness value from the simulator ranges between 0--100, however the 7-segment display requires a value between 0--15.

To adjust the range, on the **Modify** tab for the **Display brightness** configuration, add an **Interpolate** modifier. Set the input values to **0** and **100**. Set the output values to **0** and **15**.

{{< screenshot image="modify-interpolation.png" title="Screenshot of an output configuration with an Interpolate modifier added to the Modify tab." >}}

### Ensure the brightness is 0 when power is off

When the aircraft is cold and dark, the brightness sim variable may still report the actual position of the knob instead of `0`.

To address this, on the **Modify** tab for the **Display brightness** configuration, add a **Transform** modifier to multiply the brightness by the avionics power value config reference using the formula **$#**. This ensures the output brightness will be `0` when the avionics power reports `0`.

{{< screenshot image="modify-transformation.png" title="Screenshot of an output configuration with a Transform modifier added to the Modify tab." >}}

### Use the brightness output to control the display brightness

On the **Display** tab for the 7-segment display output configuration, set the **Brightness ref.** dropdown to the **Display brightness** output configuration.

{{< screenshot image="brightness-ref.png" title="Screenshot of the 7-segment display output configuration with the Display tab selected, and the Brightness ref dropdown set to Display brightness." >}}

{{% /steps %}}
