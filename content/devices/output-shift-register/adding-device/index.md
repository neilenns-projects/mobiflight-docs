---
title: Adding the device
description: Step-by-step guide for configuring a board with an output shift register in MobiFlight.
ogimage: card-images/devices/output-shift-register-dm13a.png
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the output shift register

Click on the board the device is connected to, then select **Shift Register** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Shift Register item highlighted." >}}

### Configure the output shift register

Use the **Latch**, **Clock**, and **Data** dropdowns to specify the board pins used. The pin names can vary depending on the chip variant used. Use the following mapping for the most common names:

{{< tabs items="74HC595 DIP-8,DM13A DIP-16,TLC5917 DIP-8" >}}

{{< tab >}}

| MobiFlight setting | Pin name | Pin number |
| ------------------ | -------- | ---------- |
| Latch              | RCLK     | 11         |
| Clock              | SRCLK    | 12         |
| Data               | SER      | 14         |

{{< /tab >}}

{{< tab >}}

| MobiFlight setting | Pin name | Pin number |
| ------------------ | -------- | ---------- |
| Latch              | LAT      | 4          |
| Clock              | DCK      | 3          |
| Data               | DAI      | 2          |

{{< /tab >}}

{{< tab >}}

| MobiFlight setting | Pin name | Pin number |
| ------------------ | -------- | ---------- |
| Latch              | LE(ED1)  | 4          |
| Clock              | CLK      | 3          |
| Data               | SDI      | 2          |

{{< /tab >}}

{{< /tabs >}}

Specify the number of connected chips using the **# of 8 bit registers** dropdown.

> [!TIP]
> The **# of 8 bit registers** dropdown specifies the number of 8 bit groups connected
> in series. Some chips are 8-bit, while others are 16-bit. If connecting a 16-bit chip
> set this dropdown to **2**, since that is two 8-bit groups.

Provide a meaningful name for the output shift register in the **Name** field. This name is shown in the output configuration screens when assigning the output shift register to a flight simulator output.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an output shift register, with pin 2, 3 and 4 selected, one 8-bit group, and Shift Register as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
