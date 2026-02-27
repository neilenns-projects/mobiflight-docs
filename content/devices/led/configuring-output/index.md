---
title: Configuring the output
description: Step-by-step guide for configuring an output to use an LED in MobiFlight.
ogimage: card-images/devices/led.png
weight: 30
---

LEDs are typically mapped to simulator variables that output either `0` (for off) or `1` (for on). The following steps demonstrate how to use an LED to show the current state of the parking brake in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using an LED in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new output config

Click the **Add Output Config** button in the main MobiFlight window to open the output configuration dialog.

{{< figure src="/app/new-output-config.png" alt="Screenshot of the main window with the Add Output Config button highlighted." >}}

### Filter the output presets

On the **Sim Variable** tab, use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-variable-filtered-list.png" title="Screenshot of the sim variable tab in the output dialog filtered by Microsoft / Generic / Controls." >}}

### Select the parking indicator preset

Use the **Select Preset** dropdown to select the **PARKING BRAKE INDICATOR** preset.

{{< screenshot image="sim-variable-brake-parking-indicator.png" title="Screenshot of the sim variable tab in the output dialog with the PARKING BRAKE INDICATOR preset selected." >}}

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **LED / Output** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and LED / Output type selected." >}}

### Select the LED to use for display

Use the **Select Pins** dropdown to select the [LED device](/devices/led/adding-device) that should display the output value.

{{< screenshot image="display-tab-select-pins.png" title="Screenshot of the display tab in the output dialog with an LED output selected in the select pins dropdown." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Output Event** name in the main window.

{{< screenshot image="output-config-default-name.png" title="Screenshot of the main window with the New Output Event row text highlighted." >}}

Type in a meaningful name for the new config, for example **Parking brake**, and press enter to apply the change.

{{< screenshot image="output-config-custom-name.png" title="Screenshot of the main window with Parking brake entered as a custom name." >}}

### Try out the event

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake in the simulator. The attached LED should light up when the parking brake is applied.

> [!TIP]
> Even though these steps are for a Cessna 172, the same parking brake indicator preset should work for most planes in Microsoft Flight Simulator.

{{% /steps %}}
