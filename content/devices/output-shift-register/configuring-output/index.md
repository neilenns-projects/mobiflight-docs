---
title: Configuring the output
description: Step-by-step guide for configuring an output to use an LED attached to an output shift register or LED driver in MobiFlight.
ogimage: card-images/devices/output-shift-register-dm13a.png
weight: 30
---

Devices connected to output shift registers are typically mapped to simulator variables that output either `0` (for off) or `1` (for on). The following steps demonstrate how to use an LED attached to an output shift register to show the current state of the parking brake in a Cessna 172 in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using an output shift register with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Create a new row in the outputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the output. For example, enter **Parking brake** for an LED that will show the state of the parking brake.

{{< screenshot image="output-config-highlight-new.png" title="Screenshot of the output tab in the main window with the bottom row highlighted in red." >}}

### Open the output configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="output-config-highlight-edit.png" title="Screenshot of the output tab in the main window with the edit button highlighted in red." >}}

### Filter the output presets

On the **Sim Variable** tab, use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-variable-filtered-list.png" title="Screenshot of the sim variable tab in the output dialog filtered by Microsoft / Generic / Controls." >}}

### Select the parking indicator preset

Use the **Select Preset** dropdown to select the **PARKING BRAKE INDICATOR** preset.

{{< screenshot image="sim-variable-brake-parking-indicator.png" title="Screenshot of the sim variable tab in the output dialog with the PARKING BRAKE INDICATOR preset selected." >}}

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **ShiftRegister** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and ShiftRegister type selected." >}}

### Select the LED to use for display

Use the **Shift Register** dropdown to select the [output shift register](/devices/output-shift-register/adding-device) that should display the output value. Use the **Select Pins** dropdown to select the pin on the output shift register the LED is connected to.

{{< screenshot image="display-tab-select-pins.png" title="Screenshot of the display tab in the output dialog with an output shift register selected in the Shift Register dropdown and Output 0 selected in the Select Pins dropdown." >}}

### Close the dialog and try it out

Click the **OK** button to close the dialog, then spawn an airplane in Microsoft Flight Simulator.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake in the simulator. The attached LED should light up when the parking brake is applied.

{{% /steps %}}
