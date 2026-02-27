---
title: Configuring the output
description: Step-by-step guide for configuring an output to a servo in MobiFlight.
ogimage: card-images/devices/servo.png
weight: 30
---

Servos are typically mapped to simulator variables that output numerical values, and require positive integer inputs between 0 and 255. Most simulator variables will require scaling to work properly with these servo input ranges.

The following steps demonstrate how to use a servo and MobiFlight value modifiers to display the flap position in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a servo with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Create a new row in the outputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the output. For example, enter **Flap position** for a servo that will show the current flap position.

{{< screenshot image="output-config-highlight-new.png" title="Screenshot of the output tab in the main window with the bottom row highlighted in red." >}}

### Open the output configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="output-config-highlight-edit.png" title="Screenshot of the output tab in the main window with the edit button highlighted in red." >}}

### Filter the output presets

On the **Sim Variable** tab, use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-variable-filtered-list.png" title="Screenshot of the sim variable tab in the output dialog filtered by Microsoft / Generic / Controls." >}}

### Select the flaps position preset

Use the **Select Preset** dropdown to select the **FLAPS HANDLE PERCENT** preset.

{{< screenshot image="sim-variable-flaps-percent.png" title="Screenshot of the sim variable tab in the output dialog with the FLAPS HANDLE PERCENT preset selected." >}}

### Add an interpolation modifier

On the **Modify** tab, click the **Add Modifier** button and select **Interpolation** to add a new modifier to the output configuration.

{{< screenshot image="modify-tab-add-modifier.png" title="Screenshot of the modify tab in the output dialog with the Add Modifier button menu open and Interpolation selected." >}}

### Edit the modifier

Click the **Interpolation: 2 values with Min 0 and Max 1024** text to enter edit mode.

{{< screenshot image="modify-tab-edit-modifier.png" title="Screenshot of the modify tab in the output dialog with the interpolation modifier highlighted." >}}

### Set the interpolation values

Since the value range from the simulator is **0--1** and the servo requires a value of **0--255**, set the first **Input value** row to map **0** to **0** and the second **Input Value** row to map **1** to **255**.

{{< screenshot image="modify-tab-interpolation-values.png" title="Screenshot of the modify tab in the output dialog with the interpolation modifier input values set." >}}

> [!TIP]
> The values can be inverted by mapping **0** to **255** and **1** to **0**, if necessary.

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **Servo** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and Servo type selected." >}}

### Configure the servo for display

Use the **Servo** dropdown to select the [servo](/devices/servo/adding-device/) that should display the output value. Since the modifier adjusts the flaps handle position to a value from 0--255, set the **Min. value** to **0** and the **Max. value** to **255**.

{{< screenshot image="display-tab-servo-settings.png" title="Screenshot of the display tab in the output dialog with the min value set to 0 and the max value set to 255." >}}

> [!TIP]
> To reduce the range the servo moves, adjust the **Max. rotation** value.

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Output Event** name in the main window.

{{< screenshot image="output-config-default-name.png" title="Screenshot of the main window with the New Output Event row text highlighted." >}}

Type in a meaningful name for the new config, for example **Flap position**, and press enter to apply the change.

{{< screenshot image="output-config-custom-name.png" title="Screenshot of the main window with Flap position entered as a custom name." >}}

### Try out the event

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, move the flaps handle in the simulator, and verify the servo changes position.

{{% /steps %}}

> [!TIP]
> Even though these steps are for a Cessna 172, the same flap position configuration should work for most planes in Microsoft Flight Simulator.
