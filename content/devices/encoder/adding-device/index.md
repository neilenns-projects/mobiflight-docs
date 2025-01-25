---
title: Adding the device
description: Step-by-step guide for configuring a board with an encoder in MobiFlight.
ogimage: card-images/devices/encoder-both.png
weight: 20
---

> [!TIP]
> If the encoder has an integrated button, follow the [button guide](/devices/button-switch)
> to add the button after following this guide to add the encoder.
>
> If the encoder is a dual encoder, follow this guide twice: once for the inner
> encoder and a second time for the outer encoder. Pins `A` and `B` are used when adding the first encoder,
> and pins `A'` and `B'` are used when adding the second encoder.

{{% steps %}}

### Open the MobiFlight Modules dialog

Click on the **MobiFlight Modules** button in the main window toolbar.

{{< screenshot image="/main-window-toolbar-modules.png" title="Screenshot of the MobiFlight Modules button in the main window toolbar." >}}

### Add the encoder

Click on the board the device is connected to, then select **Encoder** from the **Add device** menu.

{{< screenshot image="add-device-menu.png" title="Screenshot of the menu open with the Encoder item highlighted." >}}

### Configure the encoder

Use the **Pin settings** dropdown to specify the board pins for the left and right pins of the encoder.

Select the **Type** dropdown to specify the type of the encoder.

Provide a meaningful name for the encoder in the **Name** field. This name is shown in the input configuration screens when assigning the encoder to a flight simulator input.

> [!TIP]
> The encoder type usually isn't listed on the encoder datasheet.
> Start with **1 detent per cycle (11)** and see how well it works.
> If the encoder is missing steps when turned edit the device configuration and
> try the other three types until the encoder accurately responds to each step.

{{< screenshot image="device-configuration.png" title="Screenshot of the settings for an encoder, with pin 2 and 3 selected, type 11 selected, and Encoder as the name." >}}

### Upload the changes to the board

Click the **Upload config** button at the bottom of the **MobiFlight Modules** tab to upload the modified
configuration to the board.

{{< screenshot image="/upload-config-button.png" title="Screenshot of the MobiFlight Module dialog with the Upload config highlighted." >}}

### Close the MobiFlight modules dialog

Click the **OK** button to close the MobiFlight modules dialog and return to the main app window.

{{%/ steps %}}
