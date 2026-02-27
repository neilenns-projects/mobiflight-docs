---
title: Adding the device
description: Step-by-step guide for configuring a board with an input shift register in MobiFlight.
ogimage: card-images/devices/input-shift-register.png
weight: 20
---

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< screenshot image="/app/extras-settings-menu-item.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< screenshot src="/app/settings-modules-tab.png" title="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Add the input shift register

Click on the board the device is connected to, then select **Input Shift Register** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Input Shift Register item highlighted." >}}

### Configure the input shift register

Use the **Latch**, **Clock**, and **Data** dropdowns to specify the board pins used. The pin names can vary depending on the chip variant used. Use the following mapping for the most common names:

| MobiFlight setting | Pin name | Pin number |
| ------------------ | -------- | ---------- |
| Latch              | SH/~LD   | 1          |
| Clock              | CLK      | 2          |
| Data               | QH       | 9          |

Specify the number of chips connected in series using the **# of 8 bit registers** dropdown.

Provide a meaningful name for the input shift register in the **Name** field. This name is shown in the input configuration screens when assigning the input shift register to a flight simulator input.

> [!TIP]
> The **# of 8 bit registers** dropdown specifies the number of 8-bit groups connected in series. Some chips are 8-bit, while others are 16-bit. If connecting a 16-bit chip set this dropdown to **2**, since that is two 8-bit groups.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an input shift register, with pin 2, 3 and 4 selected, one 8-bit group, and InputShifter as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
