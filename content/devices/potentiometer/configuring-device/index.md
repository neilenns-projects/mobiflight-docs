---
title: Configuring the input
description: Step-by-step guide for configuring a potentiometer as an input in MobiFlight.
ogimage: card-images/devices/potentiometer.png
weight: 30
---

Potentiometers are typically connected to simulator variables that expect a range of values. The following steps demonstrate how to configure a potentiometer to control the throttle in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a potentiometer with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Create a new row in the inputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the input. For example, enter **Throttle** for a potentiometer that will control the throttle.

{{< screenshot image="input-config-highlight-new.png" title="Screenshot of the input tab in the main window with the bottom row highlighted in red." >}}

### Open the input configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="input-config-highlight-edit.png" title="Screenshot of the input tab in the main window with the edit button highlighted in red." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and potentiometer.

Alternatively, press the **Scan for input** button and turn the potentiometer to automatically detect and select the correct device.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and potentiometer selected." >}}

### Set the On Change action type and filter the presets list

On the **Input** tab, select the **On Change** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Engines**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Engines." >}}

### Select the throttle preset

Use the **Select Preset** dropdown to select the **THROTTLE1_SET** preset.

{{< screenshot image="input-event-throttle.png" title="Screenshot of the input tab on press event with the THROTTLE1_SET preset selected." >}}

> [!TIP]
> The `@` symbol in the event is the placeholder that gets filled with the current potentiometer value.
>
> The default **THROTTLE1_SET** preset is designed for a potentiometer with a range of 0 to 1023 and a throttle with a range of 0 to 16383. Many potentiometers provide a slightly different range. Follow the [troubleshooting guide](/devices/potentiometer/troubleshooting/) to obtain the specific range for your potentiometer.
>
> If the simulator event expects a different range use the [HubHop potentiometer tool](https://hubhop.mobiflight.com/tools/) to generate the correct custom input event.

### Close the dialog and try it out

Click the **OK** button to close the dialog, then spawn an airplane in Microsoft Flight Simulator.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try adjusting the throttle by turning the potentiometer. The throttle in the simulator should move.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same throttle event should work for most single-engine planes in Microsoft Flight Simulator.
