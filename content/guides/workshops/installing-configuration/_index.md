---
title: Installing the board configuration
description: How to install the workshop board configuration with MobiFlight.
weight: 10
---

MobiFlight workshops use a [Mega 2560 Pro Mini](/boards/recommended/mega-2560-pro-mini) board with a pre-defined device configuration. This configuration maps the devices to the appropriate pins for use with a [prototyping board v2](https://shop.mobiflight.com/product/prototyping-board-v2).

Use the following steps to upload the configuration to a board.

> [!IMPORTANT]
> These steps assume the board already has the appropriate MobiFlight firmware installed. To install the firmware follow the [flashing guide](/guides/flashing-ambiguous-boards/).

{{% steps %}}

### Open the settings dialog to edit modules

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< figure src="/app/extras-settings-menu-item.png" alt="Screenshot of the main window with the Settings menu item in the Extras menu highlighted." >}}

Then click on the **MobiFlight Modules** tab to display the modules.

{{< figure src="/app/settings-modules-tab.png" alt="Screenshot of the Settings dialog with the MobiFlight Modules tab highlighted." >}}

### Select the board

Click on the **MobiFlight Mega** board in the list of connected boards.

{{< screenshot image="mega-selected.png" title="Screenshot of the MobiFlight Modules dialog with a MobiFlight Mega board selected." >}}

### Upload the configuration

Click on the **Upload** button and select **Prototyping Board (Latest Version)**.

{{< screenshot image="upload-default-config.png" title="Screenshot of the MobiFlight Modules dialog with the Upload button selected." >}}

When prompted to confirm the upload, click **OK**.

{{% /steps %}}

After the upload completes, the board will be named **ProtoBoard-v2** and all the devices will be configured.

{{< screenshot image="configured-board.png" title="Screenshot of the MobiFlight Modules dialog with a ProtoBoard-v2 configuration loaded on a Mega 2560 Pro Mini." >}}
