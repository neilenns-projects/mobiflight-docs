---
title: Configuring the input
description: Step-by-step guide for configuring a potentiometer as an input in MobiFlight.
ogimage: card-images/devices/potentiometer.png
weight: 30
---

Potentiometers are typically connected to simulator variables that expect a range of values. The following steps demonstrate how to configure a potentiometer to control the throttle in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a potentiometer in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< figure src="/app/new-input-config.png" alt="Screenshot of the main window with the Add Input Config button highlighted." >}}

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
> The default **THROTTLE1_SET** preset is designed for a potentiometer with a range of 0--1023 and a throttle with a range of 0 to 16383. Many potentiometers provide a slightly different range. Follow the [troubleshooting guide](/devices/potentiometer/troubleshooting/) to obtain the specific range for your potentiometer.
>
> If the simulator event expects a different range, use the [HubHop potentiometer tool](https://hubhop.mobiflight.com/tools/) to generate the correct custom input event.

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Input Event** name in the main window.

{{< screenshot image="input-config-default-name.png" title="Screenshot of the main window with the Throttle row text highlighted." >}}

Type in a meaningful name for the new config, for example **Throttle**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the main window with Throttle entered as a custom name." >}}

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try adjusting the throttle by turning the potentiometer. The throttle in the simulator should move.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same throttle event should work for most single-engine planes in Microsoft Flight Simulator.
