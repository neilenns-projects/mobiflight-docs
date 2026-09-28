---
title: Adding the device
description: Step-by-step guide for configuring a board with a servo in MobiFlight
images: [card-images/devices/servo.png]
weight: 20
---

> [!IMPORTANT]
> Adding a servo to an [Arduino Uno](/boards/supported/arduino-uno/) or [Arduino Nano](/boards/recommended/arduino-nano/)
> disables the PWM capability of pin D9 and D10.

{{% steps %}}

### Open the Controller Management dialog

Click on the **Extras** menu and select **Controller Management** to open the Controller Management dialog.

{{< screenshot image="/app/extras-controller-management-menu-item.png" title="Screenshot of the Extras menu with the Controller Management menu item selected." >}}

### Add the servo

Click on the board the device is connected, then select **Servo** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Servo item highlighted." >}}

### Configure the servo

Use the **DIN line** dropdown to specify the board pin the servo is connected to.

Provide a meaningful name for the servo in the **Name** field. This name is shown in the output configuration screens when assigning the servo to a flight simulator output.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for a servo, with pin 2 selected and Servo as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
