---
title: Flashing ambiguous boards
description: Step-by-step guide to flashing ambiguous boards with MobiFlight.
images: [screenshots/ambiguous-board-warning.png]
---

When connecting a new board, MobiFlight prompts to install the software on the board to make it work with MobiFlight. In some cases
MobiFlight cannot determine the board type automatically, resulting in the following dialog:

{{< screenshot image="ambiguous-board-warning.png" title="Screenshot of the ambiguous board warning." >}}

This is most common when using Arduino clones that have a CH340G chip for serial communication. To flash the board do the following steps.

{{% steps %}}

### Acknowledge the ambiguous warning dialog

Click **OK** in the warning dialog to close it. The **MobiFlight Modules** dialog will open automatically.

{{< screenshot image="compatible-module.png" title="Screenshot of the MobiFlight Modules dialog with a compatible module showing in the list." >}}

### Install the firmware that matches the device

Right-click on the compatible module and open the **Update Firmware** menu. Select the board that matches your device.

{{< screenshot image="update-firmware-menu.png" title="Screenshot of the MobiFlight Modules dialog with the Update Firmware menu open." >}}

### Wait for the firmware upload to complete

MobiFlight will display a progress dialog during the flashing process. After it completes, the MobiFlight Modules dialog will
show the board as recognized and ready for devices.

{{< screenshot image="flash-complete.png" title="Screenshot of the MobiFlight Modules dialog with a MobiFlight Mega showing in the board list." >}}

{{% /steps %}}
