---
title: Configuring the device
description: Step-by-step guide for configuring a board with a potentiometer in MobiFlight
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the potentiometer

Click on the board the device is connected, to then select **Analog Input** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Analog Input item highlighted." >}}

### Configure the potentiometer

Use the **Pin settings** dropdown to specify the board pin the potentiometer is connected to. Only analog pins are supported.

Adjust the sensitivity using the **Sensitivity** slider. The slider controls how large a change in value must occur before MobiFlight recognizes the change.

Provide a meaningful name for the potentiometer in the **Name** field. This name is shown in the input configuration screens when assigning the potentiometer to a flight simulator input.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for a potentiometer, with pin A0 selected, medium-high sensitivity, and Analog Input as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
