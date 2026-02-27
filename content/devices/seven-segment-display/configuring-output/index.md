---
title: Configuring the output
description: Step-by-step guide for configuring an output to a 7-segment display module in MobiFlight.
ogimage: card-images/devices/seven-segment-all-three.png
weight: 30
---

7-segment display modules are typically mapped to simulator variables that output numerical values. The following steps demonstrate how to use a display module to show the COM1 active frequency with a MAX7219 display module in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using a 7-segment display module with X-Plane are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Create a new row in the outputs tab of the main window

Double-click on the bottom row where the description says **Double-click row to add new config...** and enter a description for the output. For example, enter **COM1 active frequency** for a display module that will show the current COM1 active frequency.

{{< screenshot image="output-config-highlight-new.png" title="Screenshot of the output tab in the main window with the bottom row highlighted in red." >}}

### Open the output configuration dialog

Click the button with three dots in the **Edit** column for the row created in the previous step.

{{< screenshot image="output-config-highlight-edit.png" title="Screenshot of the output tab in the main window with the edit button highlighted in red." >}}

### Filter the output presets

On the **Sim Variable** tab, use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Radio**.

{{< screenshot image="sim-variable-filtered-list.png" title="Screenshot of the sim variable tab in the output dialog filtered by Microsoft / Generic / Radio." >}}

### Select the COM 1 active frequency preset

Use the **Select Preset** dropdown to select the **COM ACTIVE FREQUENCY:index** preset.

{{< screenshot image="sim-variable-com-active-frequency.png" title="Screenshot of the sim variable tab in the output dialog with the COM ACTIVE FREQUENCY:index preset selected." >}}

### Set the radio index

Since aircraft have more than one radio, MobiFlight will show a dialog to specify the COM radio value to display. Use the dialog to specify index **1**.

{{< screenshot image="sim-variable-set-index.png" title="Screenshot of the Select Index dialog with an index of 1 set." >}}

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **Display Module** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and Display Module type selected." >}}

### Select the module to use for display

Use the **Name / Number** dropdown to select the [module](/devices/seven-segment-display/adding-device) that should display the output value. If more than one module is connected in series, use the number dropdown to specify which module in series will display the value.

{{< screenshot image="display-tab-select-name-number.png" title="Screenshot of the display tab in the output dialog with LedModule and 1 selected in the Name / Number dropdowns." >}}

### Specify the digits and decimal point for display

Use the **use display** checkboxes to specify the six digits to use for the frequency display. Use the **set decimal point** checkbox to specify where the decimal point should display.

{{< screenshot image="display-tab-use-display-checkboxes.png" title="Screenshot of the display tab in the output dialog with use display boxes one through six checked and set decimal point three checked." >}}

> [!TIP]
> Leave the number of digits dropdown set to **8** even though only six digits are used to display the frequency. This dropdown is only changed in advanced display configurations.

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Output Event** name in the main window.

{{< screenshot image="output-config-default-name.png" title="Screenshot of the main window with the New Output Event row text highlighted." >}}

Type in a meaningful name for the new config, for example **COM1 active frequency**, and press enter to apply the change.

{{< screenshot image="output-config-custom-name.png" title="Screenshot of the main window with COM1 active frequency entered as a custom name." >}}

### Try out the event

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then verify the display shows the COM1 active frequency.

{{% /steps %}}

> [!TIP]
> TM1637 display modules are configured the same way but have fewer digit and decimal pins to select from in the **Display** tab.
