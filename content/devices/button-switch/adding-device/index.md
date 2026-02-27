---
title: Adding the device
description: Step-by-step guide for configuring a board with a button in MobiFlight.
ogimage: card-images/devices/buttons-switches.png
weight: 20
---

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< figure src="/app/extras-settings-menu-item.png" alt="Screenshot of the main window with the Settings menu item in the Extras menu highlighted." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< figure src="/app/settings-modules-tab.png" alt="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Add the button or switch

Click on the board the device is connected to, then select **Button** from the **Add device** menu. The same device type is used for all button and switch variations.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Button item highlighted." >}}

### Configure the button

Use the **Pin settings** dropdown to specify the board pin the button is connected to.

Provide a meaningful name for the button in the **Name** field. This name is shown in the input configuration screens when assigning the button to a flight simulator input.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for a button, with pin 2 selected, and ParkingBrake as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

> [!TIP]
> Three-position switches are added to MobiFlight as two separate button devices. Repeat the above steps to add a second device
> that is mapped to the second pin used by the three-position switch.

{{%/ steps %}}
