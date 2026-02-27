---
title: Configuring the output
description: Step-by-step guide for configuring an output to a stepper motor in MobiFlight.
ogimage: card-images/devices/stepper-motor.png
weight: 30
---

Stepper motors are typically mapped to simulator variables that output numerical values. The following steps demonstrate how to use a 28BYJ-48 stepper motor with a ULN2003 driver to show the compass heading in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a stepper motor in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new output config

Click the **Add Output Config** button in the main MobiFlight window to open the output configuration dialog.

{{< figure src="/app/new-output-config.png" alt="Screenshot of the main window with the Add Output Config button highlighted." >}}

### Filter the output presets

On the **Sim Variable** tab, use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Miscellaneous**.

{{< screenshot image="sim-variable-filtered-list.png" title="Screenshot of the sim variable tab in the output dialog filtered by Microsoft / Generic / Miscellaneous." >}}

### Select the magnetic compass preset

Use the **Select Preset** dropdown to select the **MAGNETIC COMPASS** preset.

{{< screenshot image="sim-variable-magnetic-compass.png" title="Screenshot of the sim variable tab in the output dialog with the MAGNETIC COMPASS preset selected." >}}

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **Display Module** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and Display Module type selected." >}}

### Select the stepper motor to use for display

Use the **Stepper** dropdown to select the [stepper motor](/devices/stepper-motor/adding-device) that should display the output value.

{{< screenshot image="display-tab-select-stepper.png" title="Screenshot of the display tab in the output dialog with Stepper selected in the Stepper dropdown." >}}

### Specify the display scale

Since compass values are from 0--360, set the **Display scale** to **360** steps per revolution.

{{< screenshot image="display-tab-display-scale.png" title="Screenshot of the display tab in the output dialog with display scale set to 360." >}}

> [!TIP]
> For smoother stepper motor movement, set the **Display scale** to **3600** and use a [transform modifier](/features/modifiers/transform/) to multiply the simulator value by **10** using the **`$*10`** transform.

### Set the stepper zero position

The zero position is the position MobiFlight will reset the stepper motor to when the connection to the simulator is lost.

To set the zero position, use the **Move steps** slider and **Move** button to rotate the stepper motor to the appropriate zero position, then click the **Set Zero** button to save the location.

{{< screenshot image="display-tab-set-zero.png" title="Screenshot of the display tab in the output dialog with the Move Steps slider, Move button, and Set Zero button highlighted." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Output Config** name in the main window.

{{< screenshot image="output-config-default-name.png" title="Screenshot of the main window with the New Output Config row text highlighted." >}}

Type in a meaningful name for the new config, for example **Compass**, and press enter to apply the change.

{{< screenshot image="output-config-custom-name.png" title="Screenshot of the main window with Compass entered as a custom name." >}}

### Try out the event

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar. The stepper motor should move to match the compass heading in the simulator.

{{% /steps %}}
