---
title: Manually installing the WASM module
description: How to manually install the WASM module when automatic installation fails.
weight: 30
---

[Reinstalling the WASM module](/guides/wasm-reinstall/) is the preferred method of installing the module. However, in some cases MobiFlight cannot determine the correct install location for the module. In that situation the module can be manually installed into the flight simulator community folder.

## Find the community folder

The WASM module is installed in the flight simulator community folder. The method for determining its location depends on the version of Microsoft Flight Simulator.

{{< tabs items="Microsoft Flight Simulator 2020,Microsoft Flight Simulator 2024" >}}

{{< tab >}}

{{% steps %}}

### Enable developer mode

In flight simulator select **Options** then **General options** from the main screen. Select the **Developers** category and set **Developer mode** to **On**.

{{< screenshot image="developer-mode-2020.png" title="Screenshot of Microsoft Flight Simulator 2020 settings with developer mode set to on." >}}

### Locate the community folder

From the **Tools** menu select **Virtual File System**. Expand the **Packages Folders** section in the dialog and click the **Open Community Folder** button.

{{< screenshot image="vfs-community-folder.png" title="Screenshot of the Microsoft Flight Simulator 2020 Virtual File System developer dialog with the Open Community Folder button highlighted." >}}

A File Explorer window will open to the community folder location.

{{% /steps %}}

{{< /tab >}}

{{< tab >}}

{{% steps %}}

### Open the marketplace screen

On the main screen click the **Marketplace** button.

{{< screenshot image="marketplace-button.png" title="Screenshot of the Microsoft Flight Simulator 2024 main screen with the marketplace button highlighted." >}}

### Open My Library settings

In the marketplace select **My Library** in the top left.

{{< screenshot image="my-library.png" title="Screenshot of the Microsoft Flight Simulator 2024 marketplace screen with the My Library button highlighted." >}}

Then click the **gear icon** next to the search box to open settings.

{{< screenshot image="my-library-settings.png" title="Screenshot of the Microsoft Flight Simulator 2024 My Library screen with the gear button highlighted." >}}

### Open the community folder

{{< screenshot image="community-button.png" title="Screenshot of the Microsoft Flight Simulator 2024 My Library settings with the community folder open button highlighted." >}}

A File Explorer window will open to the community folder location.

{{% /steps %}}

{{< /tab >}}

{{< /tabs >}}

## Install the WASM module

{{% steps %}}

### Close Microsoft Flight Simulator

> [!IMPORTANT]
> The simulator must be completely closed before installing the WASM module.

### Open the MobiFlight install folder

MobiFlight is installed in the `%localappdata%\MobiFlight\MobiFlight Connector\MSFS2020-module` folder. Open that location using File Explorer.

The same WASM module is used for both versions of Microsoft Flight Simulator even though the folder is named `MSFS2020-module`.

### Copy the module to the community folder

Use File Explorer to copy the `mobiflight-event-module` folder into the community folder location found in the previous section.

{{< screenshot image="wasm-module-folder.png" title="Screenshot of the MobiFlight MSFS2020-module folder with the mobiflight-event-module folder highlighted." >}}

{{% /steps %}}

## Verify the installation

Launch Microsoft Flight Simulator and MobiFlight. Once flight simulator loads to the main screen, MobiFlight will update to show the active simulator connection in the status bar.

{{< screenshot image="wasm-ok.png" title="Screenshot of the main MobiFlight window with the sim status menu open and a green checkmark next to WASM Module (MSFS)." >}}
