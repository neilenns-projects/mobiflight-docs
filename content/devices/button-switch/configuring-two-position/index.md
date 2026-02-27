---
title: Configuring two-position switch input
description: Step-by-step guide for configuring a two-position switch as an input in MobiFlight.
ogimage: card-images/devices/switch.png
weight: 40
---

Switches are typically mapped to simulator variables that expect either `0` (for off) or `1` (for on). The following steps demonstrate how to configure a two-position switch to control the parking brake in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a switch in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< figure src="/app/new-input-config.png" alt="Screenshot of the main window with the Add Input Config button highlighted." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and switch.

Alternatively, press the **Scan for input** button and toggle the connected switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type and filter the presets list

On the **Input** tab, select the **On Press** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Controls." >}}

### Select the parking brake on preset

Use the **Select Preset** dropdown to select the **PARKING_BRAKES_ON** preset.

{{< screenshot image="input-event-parking-brakes-on.png" title="Screenshot of the input tab on press event with the PARKING_BRAKES_ON preset selected." >}}

### Configure the On Release action

Repeat steps 3 and 4 for the **On Release** tab, selecting **PARKING_BRAKES_OFF** for the preset.

{{< screenshot image="input-event-parking-brakes-off.png" title="Screenshot of the input tab on release event with the PARKING_BRAKES_OFF preset selected." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Input Config** name in the main window.

{{< screenshot image="input-config-default-name.png" title="Screenshot of the main window with the Parking brake row text highlighted." >}}

Type in a meaningful name for the new config, for example **Parking brake**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the main window with Parking brake entered as a custom name." >}}

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the switch. The parking brake in the simulator should toggle.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same parking brake input events should work for most planes in Microsoft Flight Simulator.
