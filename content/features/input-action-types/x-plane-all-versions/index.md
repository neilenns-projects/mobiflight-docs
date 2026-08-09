---
title: X-Plane (all versions)
description: How to use the X-Plane (all versions) action type with MobiFlight.
aliases:
  - /guides/input-action-types/x-plane-all-versions/
weight: 20
---

The **X-Plane (all versions)** action type is the preferred way to send events to X-Plane. It provides access to over 7,000 presets from [HubHop](https://www.hubhop.com/) to interface with many popular aircraft supported by the simulator.

> [!TIP]
> To update the HubHop event list, select the **Download Latest Presets** menu item from the **Extras** > **HubHop** menu.

{{< screenshot image="x-plane-all-versions.png" title="Screenshot of a button input with the X-Plane (all versions) action type selected." >}}

| Setting                | Description                                                                                                                   |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Filter presets by text | Provides text filtering of the HubHop presets.                                                                                |
| Filter by vendor       | Filters the list of HubHop presets by the aircraft vendor.                                                                    |
| Filter by aircraft     | Filters the list of HubHop presets by the aircraft name.                                                                      |
| Filter by system       | Filters the list of HubHop presets by the aircraft system.                                                                    |
| Preset list            | Selects the preset to send when the action type is triggered.                                                                 |
| Input type             | Specifies the type of custom preset, either **DataRef** or **Command**.                                                       |
| Path                   | Specifies the DataRef or command to invoke.                                                                                   |
| Value                  | Specifies the value to send to the simulator. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |

> [!TIP]
> To enter custom code, check the **Show Preset Code** box, select the code type from the dropdown, and enter the code in the text box. There is no need to select any values from the HubHop filtering dropdowns.
