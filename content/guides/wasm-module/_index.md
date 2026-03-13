---
title: WASM module
description: Guides to troubleshoot WASM module problems in MobiFlight.
---

The WASM module is the component MobiFlight uses to send and receive events from Microsoft Flight Simulator 2020 and Microsoft Flight Simulator 2024. If MobiFlight cannot communicate with it, a warning icon will be shown in the status bar at the bottom of the main window.

{{< screenshot image="waiting-for-wasm.png" title="Screenshot of the main MobiFlight window with the sim status menu open and a Waiting for WASM Module warning." >}}

In most cases, this problem can be resolved by [reinstalling the module](/guides/wasm-module/wasm-reinstall/). For Microsoft Flight Simulator 2024, also [verify the module is enabled](/guides/wasm-module/enable-in-msfs2024). If that fails, the module can be [installed manually](/guides/wasm-module/wasm-manual-install/).

> [!TIP]
> A project must have at least one input or output configuration that uses Microsoft Flight Simulator (SimConnect) events
> for the sim status menu to show the WASM module status.
