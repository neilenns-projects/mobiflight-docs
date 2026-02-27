---
title: Configuring button input
description: Step-by-step guide for configuring a button as an input in MobiFlight.
ogimage: card-images/devices/tactile-buttons.png
weight: 30
---

Buttons are typically mapped to simulator variables that expect either `0` (for off) or `1` (for on). The following steps demonstrate how to configure a button to toggle the parking brake in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a button in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< figure src="/app/new-input-config.png" alt="Screenshot of the main window with the Add Input Config button highlighted." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and button.

Alternatively, press the **Scan for input** button and press the connected button to automatically detect and select the correct button.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and button selected." >}}

### Set the On Press action type and filter the presets list

On the **Input** tab, select the **On Press** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Controls." >}}

### Select the parking brake toggle

Use the **Select Preset** dropdown to select the **PARKING BRAKES TOGGLE** preset.

{{< screenshot image="input-event-parking-brakes-toggle.png" title="Screenshot of the input tab on press event with the PARKING BRAKES TOGGLE preset selected." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Input Event** name in the main window.

{{< screenshot image="input-config-default-name.png" title="Screenshot of the main window with the New Input Event row text highlighted." >}}

Type in a meaningful name for the new config, for example **Parking brake**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the main window with Parking brake entered as a custom name." >}}

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the BUTTON. The parking brake in the simulator should toggle.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same parking brake input event should work for most planes in Microsoft Flight Simulator.
