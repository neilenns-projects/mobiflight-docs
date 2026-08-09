---
title: Configuring three-position switch input
description: Step-by-step guide for configuring a three-position switch as an input in MobiFlight.
images: [card-images/devices/switch-three-position.png]
weight: 50
---

<!-- Because tabs are used in this document the headings across tabs are duplicate. Disable the markdownlint -->
<!-- warning for those headings. -->
<!-- markdownlint-disable MD024 -->

Three-position switches are typically mapped to three different simulator variables that expect either `0` (for off) or `1` (for on). Despite controlling three different variables, only two input configurations are used in MobiFlight to create the mapping between the switch and simulator.

The following steps demonstrate how to configure a three-position switch to control the STBY BATT switch in a Cessna 172 in Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a switch in an X-Plane project are similar. Use the **X-Plane (All versions)** type when configuring the **Action type**.

## Configure the switch up position

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< screenshot image="/app/new-input-config.png" title="Screenshot of the main window with the Add Input Config button highlighted." >}}

### Name the config

Type in a meaningful name for the new config in the header of the dialog, for example **Standby battery - up**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name-up.png" title="Screenshot of the input config window with Standby battery - up entered as a custom name." >}}

### Select the board and device for the input

In the **Trigger** section, use the **Select controller...** and **Select device...** dropdowns to select your connected board and switch.

Alternatively, press the **Scan for input** button and toggle the switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected-up.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type

In the **Actions** section, select the **On Press** button. Use the **Action Type** dropdown to select **Microsoft Flight Simulator (all versions)**.

{{< screenshot image="action-type-up.png" title="Screenshot of the input config dialog with the action type set to Microsoft Flight Simulator (all versions)." >}}

### Filter the presets list

Use the **Select preset** dropdowns to filter by **Microsoft**, **C172 (2024)**, and **Electrical**.

{{< screenshot image="sim-events-filtered-list-up.png" title="Screenshot of the on press filter preset list filtered by Microsoft / C172 (2024) / Electrical." >}}

### Select the standby battery arm preset

Use the preset list to select the **Standby battery - Arm** preset, then click **Go back**.

{{< screenshot image="input-event-standby-battery-arm.png" title="Screenshot of the input config on press event with the Standby battery - Arm preset selected." >}}

### Configure the On Release action

Repeat steps 4 through 6 for the **On Release** action, selecting **Standby battery - Off** for the preset.

> [!NOTE]
> For three-position switches, the **On Release** event is always set to the event that maps to the middle switch position.

{{< screenshot image="input-event-standby-battery-off-up.png" title="Screenshot of the input config on release event with the Standby battery - off preset selected." >}}

### Close the dialog

Click the **Apply changes** button to close the dialog, then configure the switch down position.

{{% /steps %}}

## Configure the switch down position

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< screenshot image="/app/new-input-config.png" title="Screenshot of the main window with the Add Input Config button highlighted." >}}

### Name the config

Type in a meaningful name for the new config in the header of the dialog, for example **Standby battery - down**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name-down.png" title="Screenshot of the input config window with Standby battery - down entered as a custom name." >}}

### Select the board and device for the input

In the **Trigger** section, use the **Select controller...** and **Select device...** dropdowns to select your connected board and switch.

Alternatively, press the **Scan for input** button and toggle the switch to automatically detect and select the correct switch.

{{< screenshot image="input-selected-down.png" title="Screenshot of the input configuration dialog with a board and switch selected." >}}

### Set the On Press action type

In the **Actions** section, select the **On Press** button. Use the **Action Type** dropdown to select **Microsoft Flight Simulator (all versions)**.

{{< screenshot image="action-type-down.png" title="Screenshot of the input config dialog with the action type set to Microsoft Flight Simulator (all versions)." >}}

### Filter the presets list

Use the **Select preset** dropdowns to filter by **Microsoft**, **C172 (2024)**, and **Electrical**.

{{< screenshot image="sim-events-filtered-list-down.png" title="Screenshot of the on press filter preset list filtered by Microsoft / C172 (2024) / Electrical." >}}

### Select the standby battery test preset

Use the **Select Preset** dropdown to select the **Standby battery - Test** preset, then click **Go back**.

{{< screenshot image="input-event-standby-battery-test.png" title="Screenshot of the input config on press event with the Standby battery - Test preset selected." >}}

### Configure the On Release action

Repeat steps 4 through 6 for the **On Release** action, selecting **Standby battery - Off** for the preset.

> [!NOTE]
> For three-position switches, the **On Release** event is always set to the event that maps to the middle switch position.

{{< screenshot image="input-event-standby-battery-off-down.png" title="Screenshot of the input config on release event with the Standby battery - off preset selected." >}}

### Close the dialog

Click the **Apply changes** button to close the dialog.

{{% /steps %}}

## Try out the events

After configuring both inputs, spawn an airplane in Microsoft Flight Simulator.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try moving the switch to the three different positions to control the standby battery switch. The switch in the simulator should move to match the physical switch position.

> [!NOTE]
> When activating the **TEST** position, the switch in the simulator will automatically return to the **OFF** position after a short delay. This is expected, as the simulator treats the **TEST** position as a momentary switch.
