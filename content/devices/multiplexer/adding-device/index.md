---
title: Adding the device
description: Step-by-step guide for configuring a board with a multiplexer in MobiFlight.
ogimage: card-images/devices/multiplexer.png
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the multiplexer

Click on the board the device is connected to, then select **Digital Input Multiplexer** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Digital Input Multiplexer item highlighted." >}}

### Configure the multiplexer

Use the **S0**, **S1**, **S2** and **S3** dropdowns to specify the board pins used. Set the **Data** dropdown to the board pin connected to the **SIG** pin on the breakout board.

Specify the size of the multiplexer using the **Type** dropdown. Use **8-bit multiplexer** for 74HC4051 chips and **16-bit multiplexer** for 74HC4067 chips.

Provide a meaningful name for the multiplexer in the **Name** field. This name is shown in the input configuration screens when assigning the multiplexer to a flight simulator input.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for a 74HC4067 multiplexer, with pin 2, 3, 4, and 5 selected, data pin 12, 16-bit multiplexer, and Multiplexer as the name." >}}

> [!TIP]
> When connecting additional multiplexer to the same board, they can share the **S0--S3** pins. Each multiplexer must use a dedicated **Data** pin.

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
