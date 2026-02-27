---
title: Configuring the input
description: Step-by-step guide for configuring an encoder as an input in MobiFlight.
ogimage: card-images/devices/encoder-single.png
weight: 30
---

Encoders are typically mapped to simulator variables that increase and decrease in value. The following steps demonstrate how to configure a single encoder to adjust the Cessna 172 autopilot heading value in Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024.

> [!TIP]
> The steps for using an encoder in an X-Plane project are similar. Use the **X-Plane DataRef** type when configuring the **Sim Variable** tab.

{{% steps %}}

### Add a new input config

Click the **Add Input Config** button in the main MobiFlight window to open the input configuration dialog.

{{< figure src="/app/new-input-config.png" alt="Screenshot of the main window with the Add Input Config button highlighted." >}}

### Select the board and device for the input

On the **Input** tab, use the **Module** and **Device** dropdowns to select your connected board and encoder.

Alternatively, press the **Scan for input** button and rotate the encoder to automatically detect and select the correct encoder.

{{< screenshot image="input-selected.png" title="Screenshot of the input configuration dialog with a board and encoder selected." >}}

### Set the On Left action type and filter the presets list

On the **Input** tab, select the **On Left** input setting tab. Use the **Action Type** dropdown to select **Microsoft Flight Simulator**. Then use the **Filter Preset List** dropdowns to filter by **Microsoft**, **Generic**, and **Controls**.

{{< screenshot image="sim-events-filtered-list.png" title="Screenshot of the on press filter preset list filtered by Microsoft / Generic / Controls." >}}

### Select the heading decrement preset

Use the **Select Preset** dropdown to select the **AP_HDG_VAR_DEC** preset.

{{< screenshot image="input-event-heading-decrement.png" title="Screenshot of the input tab on press event with the AP_HDG_VAR_DEC preset selected." >}}

### Configure the On Right action

Repeat steps 3 and 4 for the **On Right** tab, selecting **AP_HDG_VAR_INC** for the preset.

{{< screenshot image="input-event-heading-increment.png" title="Screenshot of the input tab on release event with the AP_HDG_VAR_INC preset selected." >}}

### Close the dialog and name the config

Click the **OK** button to close the dialog, then double-click on the **New Input Config** name in the main window.

{{< screenshot image="input-config-default-name.png" title="Screenshot of the main window with the AP - Heading row text highlighted." >}}

Type in a meaningful name for the new config, for example **AP - Heading**, and press enter to apply the change.

{{< screenshot image="input-config-custom-name.png" title="Screenshot of the main window with AP - Heading entered as a custom name." >}}

### Try out the event

Launch Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar, then try adjusting the autopilot heading with the encoder. The heading value in the simulator should increment and decrement.

{{% /steps %}}

<!-- markdownlint-disable MD028 -->
<!-- markdownlint doesn't know that these are two separate GitHub alert boxes. -->

> [!TIP]
> Even though these steps are for a Cessna 172, the same heading input events should work for most planes in Microsoft Flight Simulator.

> [!TIP]
> If the encoder triggers the opposite event, where rotating clockwise activates the **On Left** event, it means the pins
> were configured backwards in the **MobiFlight Modules** dialog. To fix this, [edit the device in the **MobiFlight Modules** dialog](/devices/encoder/adding-device/)
> and press the **Swap** button to swap the pin assignments for the left and right pin.

<!-- markdownlint-enable MD028 -->
