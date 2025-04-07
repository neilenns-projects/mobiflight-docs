---
title: Controlling 7-segment brightness
description: How to control 7-segment display brightness with an output variable.
---

7-segment displays can have their brightness set using the value of an output configuration. This is most often used to turn the displays off and on based on an airplane's master battery switch.

The following steps demonstrate how to use an airplane's master battery switch state in a Cessna 172 to turn a MAX7219 display module off and on in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!NOTE]
> This guide assumes an [output configuration](/devices/seven-segment-display/configuring-output/) is already created to display a value on the display.

{{% steps %}}

### Create an output configuration for the brightness

Add an output configuration named **Display brightness**. Select the **ELECTRICAL MASTER BATTERY** preset, and when prompted set the index to **2**.

This preset is `0` when the master battery is off and `1` when the master battery is on.

{{< screenshot image="display-brightness-output-config.png" title="Screenshot of an output configuration with the ELECTRICAL MASTER BATTERY preset highlighted." >}}

> [!TIP]
> The index value will vary depending on the aircraft.

### Add a transform modifier to battery output

On the **Modify** tab for the output created in the previous step, add a [**Transform** modifier](/features/modifiers/transform/) and set the value to `$*5`. This multiplies the value from the simulator (either `0` or `1`) by five to provide a brightness value of `5` when the master battery is on.

{{< screenshot image="display-brightness-modify.png" title="Screenshot of an output configuration with the Modify tab selected and a transform modifier added." >}}

> [!TIP]
> 7-segment displays support 1--15 for brightness values. Adjust the brightness of the display when on by changing `5` to the desired brightness level.

### Add a config reference to the 7-segment display configuration

Edit the output configuration for the 7-segment display. On the **Modify** tab, click the **Add Reference** button to add the output configuration defined in the previous step.

{{< screenshot image="modify-config-reference.png" title="Screenshot of the 7-segment display output configuration with the Modify tab selected, and the Display brightness output configuration added." >}}

### Use the config reference to control the brightness

On the **Display** tab for the 7-segment display output configuration, set the **Brightness ref.** dropdown to the output added on the **Modify** tab.

{{< screenshot image="brightness-ref.png" title="Screenshot of the 7-segment display output configuration with the Display tab selected, and the Brightness ref dropdown set to Display brightness." >}}

{{% /steps %}}
