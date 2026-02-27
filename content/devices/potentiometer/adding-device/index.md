---
title: Adding the device
description: Step-by-step guide for configuring a board with a potentiometer in MobiFlight
ogimage: card-images/devices/potentiometer.png
weight: 20
---

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< screenshot image="/app/extras-settings-menu-item.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< screenshot src="/app/settings-modules-tab.png" title="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Add the potentiometer

Click on the board the device is connected, then select **Analog Input** from the **Add device** menu.

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
