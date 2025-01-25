---
title: Reinstalling the WASM module
description: How to reinstall the WASM module with MobiFlight.
weight: 20
---

In most cases this problem can be resolved by reinstalling the module.

{{% steps %}}

### Close Microsoft Flight Simulator

> [!IMPORTANT]
> The simulator must be completely closed before installing the WASM module.

### Run the installer

In the main MobiFlight window go to the **Extras** menu and select **Microsoft Flight Simulator** then **Install WASM Module**.

{{< screenshot image="install-wasm-menu.png" title="Screenshot of the main MobiFlight window with the Extras menu, Microsoft Flight Simulator submenu, and Install WASM Module menu item selected." >}}

A dialog will show after the installation completes indicating a successful install.

{{< screenshot image="success-dialog.png" title="Screenshot of the main MobiFlight window with a dialog showing a successful WASM installation." >}}

{{% /steps %}}

## Verify the installation

Launch Microsoft Flight Simulator and MobiFlight. Once flight simulator loads to the main screen, MobiFlight will update to show the active simulator connection in the status bar.

{{< screenshot image="wasm-ok.png" title="Screenshot of the main MobiFlight window with the sim status menu open and a green checkmark next to WASM Module (MSFS)." >}}

> [!TIP]
> In some instances the automatic installation will fail with an error stating the community folder could not be located.
> If that happens follow the [manual WASM installation guide](/guides/wasm-module/wasm-manual-install/).
