---
title: Configuring the output
description: Step-by-step guide for configuring an output to an LCD in MobiFlight.
ogimage: card-images/devices/lcd-20x4.png
weight: 30
---

LCDs are typically mapped to simulator variables that output numerical values. The following steps demonstrate how to use a display to show the COM1 active frequency heading in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024. See the [advanced configuration](/devices/lcd/advanced-configuration/) guide for steps to show more than one simulator value on the display at a time.

> [!TIP]
> The steps for using an LCD in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new output config

Click the **Add Output Config** button in the main MobiFlight window to open the output configuration dialog.

{{< screenshot image="/app/new-output-config.png" title="Screenshot of the main window with the Add Output Config button highlighted." >}}

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

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **LcdDisplay** device type.

{{< screenshot image="display-tab-output-selected.png" title="Screenshot of the display tab in the output dialog with a board and LcdDisplay type selected." >}}

### Select the module to use for display

Use the **Display** dropdown to select the [module](/devices/lcd/adding-device) that should display the output value. If more than one module is connected in series, use the number dropdown to specify which module in series will display the value.

{{< screenshot image="display-tab-device-selected.png" title="Screenshot of the display tab in the output dialog with LcdDisplay selected in the Display dropdown." >}}

### Format the display output

Replace the **Text** section sample text with `$$$.$$$` to indicate six digits should be displayed with a decimal after the third digit.

{{< screenshot image="display-tab-formatted-output.png" title="Screenshot of the display tab in the output dialog with the Text field filled $$$.$$$." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Output Config** name in the main window.

{{< screenshot image="output-config-default-name.png" title="Screenshot of the main window with the New Output Config row text highlighted." >}}

Type in a meaningful name for the new config, for example **COM1 active frequency**, and press enter to apply the change.

{{< screenshot image="output-config-custom-name.png" title="Screenshot of the main window with COM1 active frequency entered as a custom name." >}}

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then verify the display shows the COM1 active frequency.

{{% /steps %}}
