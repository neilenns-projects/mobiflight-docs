---
title: Adding the device
description: Step-by-step guide for configuring a board with a stepper motor in MobiFlight.
ogimage: card-images/devices/stepper-motor.png
weight: 20
---

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the stepper motor

Click on the board the device is connected to, then select **Stepper** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Stepper item highlighted." >}}

### Configure the stepper motor

{{< tabs items="28BYJ-48 with ULN2003 driver,Nema 17 with TB6600 driver" >}}

{{< tab >}}

In the **Additional settings** section, select the **28BYJ - Half-step mode (recommended)** preset.

Set the **Pin 1**, **Pin 2**, **Pin 3**, and **Pin 4** dropdowns to the board pins connected to the **IN1--IN4** pins on the driver board.

Provide a meaningful name for the stepper in the **Name** field. This name is shown in the output configuration screens when assigning the stepper to a flight simulator output.

{{< screenshot image="device-configuration-28BYJ-half-step-mode.png" title="Screenshot of the settings for a stepper motor, with pin 2, 3, 4, and 5 selected, Stepper as the name, and the 28BYJ - Half-step mode (recommended) preset selected." >}}

{{< /tab >}}

{{< tab >}}

In the **Additional settings** section, select the **Generic - EasyDriver** preset.

Set **Pin 1** to the board pin connected to the **PUL-** pin on the driver board. Set **Pin 2** to the board pin connected to the **DIR-** pin on the driver board.

Provide a meaningful name for the stepper in the **Name** field. This name is shown in the output configuration screens when assigning the stepper to a flight simulator output.

{{< screenshot image="device-configuration-generic-easy-driver.png" title="Screenshot of the settings for a stepper motor, with pin 2 and 3, Stepper as the name, and the Generic - EasyDriver preset selected." >}}

{{< /tab >}}

{{< /tabs >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
