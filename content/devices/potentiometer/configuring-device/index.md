---
title: Configuring the input
description: Step-by-step guide for configuring a potentiometer as an input in MobiFlight.
images: [card-images/devices/potentiometer.png]
weight: 30
---

Potentiometers are typically connected to simulator variables that expect a range of values. The following steps demonstrate how to configure a potentiometer to control the throttle in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a potentiometer in an X-Plane project are similar. Use the **X-Plane (All versions)** type when configuring the **Action type**.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< screenshot image="/app/new-input-config.png" title="Screenshot of the main window with the Add Input Config button highlighted." >}}

## Name the config

Type in a meaningful name for the new config in the header of the dialog, for example **Throttle**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the input config with trottle entered as a custom name." >}}

### Select the board and device for the input

In the **Trigger** section, use the **Select controller...** and **Select device...** dropdowns to select your connected board and potentiometer.

Alternatively, press the **Scan for input** button and rotate the potentiometer to automatically detect and select the correct potentiometer.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and analog input selected." >}}

### Set the On Change action type

In the **Actions** section, select the **On Change** button. Use the **Action Type** dropdown to select **Microsoft Flight Simulator (all versions)**.

{{< screenshot image="action-type.png" title="Screenshot of the input config dialog with the action type set to Microsoft Flight Simulator (all versions)." >}}

### Filter the presets list

Use the **Select preset** dropdowns to filter by **Microsoft**, **Generic**, and **Engines**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Engines." >}}

### Select the THROTTLE1_SET preset

Use the preset list to select the **THROTTLE1_SET** preset, then click **Go back**.

{{< screenshot image="input-event-throttle.png" title="Screenshot of the preset list with the THROTTLE1_SET preset selected." >}}

> [!TIP]
> The `@` symbol in the event is the placeholder that gets filled with the current potentiometer value.
>
> The default **THROTTLE1_SET** preset is designed for a potentiometer with a range of 0--1023 and a throttle with a range of 0 to 16383. Many potentiometers provide a slightly different range. Follow the [troubleshooting guide](/devices/potentiometer/troubleshooting/) to obtain the specific range for your potentiometer.
>
> If the simulator event expects a different range, use the [HubHop potentiometer tool](https://hubhop.mobiflight.com/tools/) to generate the correct custom input event.

### Close the dialog and try out the event

Click the **Apply changes** button to close the dialog.

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try adjusting the throttle by turning the potentiometer. The throttle in the simulator should move.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same throttle event should work for most single-engine planes in Microsoft Flight Simulator.
