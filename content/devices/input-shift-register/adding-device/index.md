---
title: Adding the device
description: Step-by-step guide for configuring a board with an input shift register in MobiFlight.
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the input shift register

Click on the board the device is connected to, then select **Input Shift Register** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Input Shift Register item highlighted." >}}

### Configure the input shift register

Use the **Latch**, **Clock**, and **Data** dropdowns to specify the board pins used. The pin names can vary depending on the chip variant used. Use the following mapping for the most common names:

| MobiFlight Setting | 74HC165 input | 74HC165 pin |
| ------------------ | ------------- | ----------- |
| Latch              | SH/~LD        | 1           |
| Clock              | CLK           | 2           |
| Data               | QH            | 9           |

Specify the number of connected chips using the **# of 8 bit registers** dropdown.

Provide a meaningful name for the input shift register in the **Name** field. This name is shown in the input configuration screens when assigning the input shift register to a flight simulator input.

> [!TIP]
> The **# of 8 bit registers** dropdown specifies the number of 8 bit groups connected
> in series. Some chips are 8-bit, while others are 16-bit. If connecting a 16-bit chip
> set this dropdown to **2**, since that is two 8-bit groups.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an input shift register, with pin 2, 3 and 4 selected, one 8-bit group, and InputShifter as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
