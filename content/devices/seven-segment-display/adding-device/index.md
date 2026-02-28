---
title: Adding the device
description: Step-by-step guide for adding an LED display module in MobiFlight.
ogimage: card-images/devices/seven-segment-all-three.png
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the display module

Click on the board the device is connected to, then select **LED 7-Segment** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the LED 7-Segment item highlighted." >}}

### Configure the display

{{< tabs >}}

{{< tab name="MAX7219" >}}

Select **MAX7219 / MAX7221** from the **Type** dropdown.

Use the **DIN**, **CS**, and **CLK** dropdowns to specify the board pins used. Specify the number of display modules connected in series using the **Num** dropdown.

Provide a meaningful name for the display module in the **Name** field. This name is shown in the output configuration screens when assigning the display to a flight simulator output.

{{< screenshot image="device-configuration-max7219.png" title="Screenshot of the settings for a MAX7219 display module, with pin 2, 3 and 4 selected, 1 module, and LedModule as the name." >}}

{{< /tab >}}

{{< tab name="TM1637 4-digit" >}}

Select **TM1637 - 4 digits** from the **Type** dropdown.

Use the **DIN** and **CLK** dropdowns to specify the board pins used. The **DIN** dropdown maps to the **DIO** pin on the display module.

Provide a meaningful name for the display module in the **Name** field. This name is shown in the output configuration screens when assigning the display to a flight simulator output.

{{< screenshot image="device-configuration-tm1637-four-digits.png" title="Screenshot of the settings for a TM1637 4-digit display module, with pin 2 and 3 selected, and LedModule as the name." >}}

{{< /tab >}}

{{< tab name="TM1637 6-digit" >}}

Select **TM1637 - 6 digits** from the **Type** dropdown.

Use the **DIN** and **CLK** dropdowns to specify the board pins used. The **DIN** dropdown maps to the **DIO** pin on the display module.

Provide a meaningful name for the display module in the **Name** field. This name is shown in the output configuration screens when assigning the display to a flight simulator output.

{{< screenshot image="device-configuration-tm1637-six-digits.png" title="Screenshot of the settings for a TM1637 6-digit display module, with pin 2 and 3 selected, and LedModule as the name." >}}

{{< /tab >}}

{{< /tabs >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
