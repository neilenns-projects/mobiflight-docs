---
title: Adding the device
description: Step-by-step guide for configuring a board with an LED in MobiFlight.
ogimage: card-images/devices/led.png
weight: 20
---

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< screenshot image="/app/extras-settings-menu-item.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< screenshot src="/app/settings-modules-tab.png" title="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Add the LED

Click on the board the device is connected to, then select **LED / Output** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the LED / Output item highlighted." >}}

### Configure the LED

Use the **Pin settings** dropdown to specify the board pin the LED is connected to.

Provide a meaningful name for the LED in the **Name** field. This name is shown in the output configuration screens when assigning a flight simulator value to the LED.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an LED, with pin 2 selected and Output as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified
configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
