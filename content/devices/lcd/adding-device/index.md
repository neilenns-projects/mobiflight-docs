---
title: Adding the device
description: Step-by-step guide for configuring an LCD with MobiFlight.
ogimage: card-images/devices/lcd-20x4.png
weight: 20
---

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< figure src="/app/extras-settings-menu-item.png" alt="Screenshot of the main window with the Settings menu item in the Extras menu highlighted." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< figure src="/app/settings-modules-tab.png" alt="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Configure the display

Use the **Display settings** to set the address for the display. Use the **Columns** and **Lines** fields to specify the number of columns and rows for the connected display.

Provide a meaningful name for the display in the **Name** field. This name is shown in the output configuration screens when assigning the display to flight simulator outputs.

> [!TIP]
> Most displays have a default address of 0x27. To change the display address, solder resistors to the available A0--A2 pads on the driver board.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an LCD, with address 0x27, 16 columns, and two lines." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
