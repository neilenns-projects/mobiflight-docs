---
title: Configuring three-position switch input
description: Step-by-step guide for configuring a three-position switch as an input in MobiFlight.
ogimage: card-images/devices/switch-three-position.png
weight: 50
---

<!-- Because tabs are used in this document the headings across tabs are duplicate. Disable the markdownlint -->
<!-- warning for those headings. -->
<!-- markdownlint-disable MD024 -->

Three-position switches are typically mapped to three different simulator variables that expect either `0` (for off) or `1` (for on). Despite controlling three different variables, only two input configurations are used in MobiFlight to create the mapping between the switch and simulator.

The following steps demonstrate how to configure a three-position switch to control the STBY BATT switch in a Cessna 172 in Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a switch with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{< tabs items="Switch up position,Switch down position" >}}

{{< tab >}}

{{% steps %}}

### Create a new row in the inputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the input. For example, enter **Standby battery - up** for a switch that will control the standby battery switch up position.

{{< screenshot image="input-config-highlight-new.png" title="Screenshot of the input tab in the main window with the bottom row highlighted in red." >}}

### Open the input configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="input-config-highlight-edit-up.png" title="Screenshot of the input tab in the main window with the edit button highlighted in red." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and switch.

Alternatively, press the **Scan for input** button and toggle the connected switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected-up.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type and filter the presets list

On the **Input** tab, select the **On Press** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **C172 (2024)**, and **Electrical**.

{{< screenshot image="sim-events-filtered-list-up.png" title="Screenshot of the on press filter preset list filtered by Microsoft / C172 (2024) / Electrical." >}}

### Select the standby battery arm preset

Use the **Select Preset** dropdown to select the **Standby battery - Arm** preset.

{{< screenshot image="input-event-standby-battery-arm.png" title="Screenshot of the input tab on press event with the Standby battery - Arm preset selected." >}}

### Configure the On Release action

Repeat steps 4 and 5 for the **On Release** tab, selecting **Standby battery - Off** for the preset.

> [!NOTE]
> For three-position switches, the **On Release** event is always set to the event that maps to the middle switch position.

{{< screenshot image="input-event-standby-battery-off-up.png" title="Screenshot of the input tab on release event with the Standby battery - off preset selected." >}}

{{% /steps %}}

{{< /tab >}}

{{< tab >}}

{{% steps %}}

### Create a new row in the inputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the input. For example, enter **Standby battery - down** for a switch that will control the standby battery switch down position.

### Open the input configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="input-config-highlight-edit-down.png" title="Screenshot of the input tab in the main window with the edit button highlighted in red." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and switch.

Alternatively, press the **Scan for input** button and toggle the connected switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected-down.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type and filter the presets list

On the **Input** tab, select the **On Press** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **C172 (2024)**, and **Electrical**.

{{< screenshot image="sim-events-filtered-list-down.png" title="Screenshot of the on press filter preset list filtered by Microsoft / C172 (2024) / Electrical." >}}

### Select the standby battery test preset

Use the **Select Preset** dropdown to select the **Standby battery - Test** preset.

{{< screenshot image="input-event-standby-battery-test.png" title="Screenshot of the input tab on press event with the Standby battery - Test preset selected." >}}

### Configure the On Release action

Repeat steps 4 and 5 for the **On Release** tab, selecting **Standby battery - Off** for the preset.

> [!NOTE]
> For three-position switches, the **On Release** event is always set to the event that maps to the middle switch position.

{{< screenshot image="input-event-standby-battery-off-down.png" title="Screenshot of the input tab on release event with the Standby battery - off preset selected." >}}

{{% /steps %}}

{{< /tab >}}

{{< /tabs >}}

## Try it out

After configuring both inputs, spawn an airplane in Microsoft Flight Simulator.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try moving the switch to the three different positions to control the standby battery switch. The switch in the simulator should move to match the physical switch position.

> [!NOTE]
> When activating the **TEST** position, the switch in the simulator will automatically return to the **OFF** position after a short delay. This is expected, as the simulator treats the **TEST** position as a momentary switch.
