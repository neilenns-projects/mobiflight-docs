---
title: Configuring the input
description: Step-by-step guide for configuring switches connected to an input shift register as an input in MobiFlight.
ogimage: card-images/devices/switch.png
weight: 30
---

Switches and buttons connected to input shift registers are typically mapped to simulator variables that expect either `0` (for off) or `1` (for on). The following steps demonstrate how to configure a two-position switch connected to an input shift register to control the parking brake in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a switch or button with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Create a new row in the inputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the input. For example, enter **Parking brake** for a switch that will control the parking brake.

{{< screenshot image="input-config-highlight-new.png" title="Screenshot of the input tab in the main window with the bottom row highlighted in red." >}}

### Open the input configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="input-config-parking-brake-highlight-edit.png" title="Screenshot of the input tab in the main window with the edit button highlighted in red." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and input shift register. Use the dropdown next to the **Device** dropdown to select the pin on the input shifter the switch is connected to.

Alternatively, press the **Scan for input** button and toggle the connected switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type and filter the presets list

On the **Input** tab, select the **On Press** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Controls." >}}

### Select the parking brake on preset

Use the **Select Preset** dropdown to select the **PARKING_BRAKES_ON** preset.

{{< screenshot image="input-event-parking-brakes-on.png" title="Screenshot of the input tab on press event with the PARKING_BRAKES_ON preset selected." >}}

### Configure the On Release action

Repeat steps 4 and 5 for the **On Release** tab, selecting **PARKING_BRAKES_OFF** for the preset.

{{< screenshot image="input-event-parking-brakes-off.png" title="Screenshot of the input tab on release event with the PARKING_BRAKES_OFF preset selected." >}}

### Close the dialog and try it out

Click the **OK** button to close the dialog, then spawn an airplane in Microsoft Flight Simulator.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the switch. The parking brake in the simulator should toggle.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same parking brake input events should work for most planes in Microsoft Flight Simulator.
