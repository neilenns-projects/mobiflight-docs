---
title: Configuring the input
description: Step-by-step guide for configuring switches connected to an input shift register as an input in MobiFlight.
images: [card-images/devices/switch.png]
weight: 30
---

Switches and buttons connected to input shift registers are typically mapped to simulator variables that expect either `0` (for off) or `1` (for on). The following steps demonstrate how to configure a two-position switch connected to an input shift register to control the parking brake in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a switch or button in an X-Plane project are similar. Use the **X-Plane (All versions)** type when configuring the **Action type**.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< screenshot image="/app/new-input-config.png" title="Screenshot of the main window with the Add Input Config button highlighted." >}}

## Name the config

Type in a meaningful name for the new config in the header of the dialog, for example **Parking brake**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the input config with parking brake entered as a custom name." >}}

### Select the board and device for the input

In the **Trigger** section, use the **Select controller...** and **Select device...** dropdowns to select your connected board and shift register pin with the connected button. Each shift register pin appears as a separate entry in the dropdown, with the pin number separated from the shift register name by a `:`.

Alternatively, press the **Scan for input** button and press the button to automatically detect and select the correct button.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and shift register pin InputShifter:0 selected." >}}

### Set the On Press action type

In the **Actions** section, select the **On Press** button. Use the **Action Type** dropdown to select **Microsoft Flight Simulator (all versions)**.

{{< screenshot image="action-type.png" title="Screenshot of the input config dialog with the action type set to Microsoft Flight Simulator (all versions)." >}}

### Filter the presets list

Use the **Select preset** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Controls." >}}

### Select the PARKING_BRAKES_ON preset

Use the preset list to select the **PARKING_BRAKES_ON** preset, then click **Go back**.

{{< screenshot image="input-event-parking-brakes-on.png" title="Screenshot of preset list with the PARKING_BRAKES_ON preset selected." >}}

### Configure the On Release action

Repeat steps 4 through 6 for the **On Release** action, selecting **PARKING_BRAKES_OFF** for the preset.

{{< screenshot image="input-event-parking-brakes-off.png" title="Screenshot of the input tab on release event with the PARKING_BRAKES_OFF preset selected." >}}

### Close the dialog and try out the event

Click the **Apply changes** button to close the dialog.

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the button. The parking brake in the simulator should toggle.

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the switch. The parking brake in the simulator should toggle.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same parking brake input events should work for most planes in Microsoft Flight Simulator.
