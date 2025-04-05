---
title: Microsoft Flight Simulator
description: How to use the Microsoft Flight Simulator action type with MobiFlight.
aliases:
  - /guides/input-action-types/microsoft-flight-simulator/
weight: 10
---

The **Microsoft Flight Simulator** action type is the preferred way to send events to Microsoft Flight Simulator 2020 and 20204. It provides access to over 20,000 presets from [HubHop](https://www.hubhop.com/) to interface with nearly every aircraft supported by the simulator.

> [!TIP]
> To update the HubHop event list, select the **Download Latest Presets** menu item from the **Extras** > **HubHop** menu.

{{< tabs items="Default view,Custom preset code view" >}}

{{< tab >}}

{{< screenshot image="msfs-default.png" title="Screenshot of a button input with the Microsoft Flight Simulator action type selected." >}}

{{< /tab >}}

{{< tab >}}

{{< screenshot image="x-plane-show-preset-code.png" title="Screenshot of a button input with the X-Plane (all versions) action type selected and the Show Preset Code checkbox checked. " >}}

{{< /tab >}}

{{< /tabs >}}

| Setting          | Description                                                                        |
| ---------------- | ---------------------------------------------------------------------------------- |
| Search           | Provides text filtering of the HubHop presets.                                     |
| Vendor           | Filters the list of HubHop presets by the aircraft vendor.                         |
| Aircraft         | Filters the list of HubHop presets by the aircraft name.                           |
| System           | Filters the list of HubHop presets by the aircraft system.                         |
| Select Preset    | Selects the preset to send when the input action is triggered.                     |
| Description      | Displays the preset description from HubHop.                                       |
| Show Preset Code | Shows the preset code and enables editing the code to create a custom input event. |
| +                | Expands the preset code text box to enable multi-line editing.                     |

> [!TIP]
> To enter custom event code, check the **Show Preset Code** box and enter the code in the preset code text box. There is no need to select any values from the HubHop filtering dropdowns.
