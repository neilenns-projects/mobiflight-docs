---
title: X-Plane (all versions)
description: How to use the X-Plane (all versions) action type with MobiFlight.
weight: 20
---

The **X-Plane (all versions)** action type is the preferred way to send events to X-Plane. It provides access to over 7,000 presets from [HubHop](https://www.hubhop.com/) to interface with many popular aircraft supported by the simulator.

> [!TIP]
> To update the HubHop event list, select the **Download Latest Presets** menu item from the **Extras** > **HubHop** menu.

{{< tabs items="Default view,Custom preset code view" >}}

{{< tab >}}

{{< screenshot image="x-plane-all-versions.png" title="Screenshot of a button input with the X-Plane (all versions) action type selected." >}}

{{< /tab >}}

{{< tab >}}

{{< screenshot image="x-plane-show-preset-code.png" title="Screenshot of a button input with the X-Plane (all versions) action type selected." >}}

{{< /tab >}}

{{< /tabs >}}

| Setting          | Description                                                                                                                   |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Search           | Provides text filtering of the HubHop presets.                                                                                |
| Vendor           | Filters the list of HubHop presets by the aircraft vendor.                                                                    |
| Aircraft         | Filters the list of HubHop presets by the aircraft name.                                                                      |
| System           | Filters the list of HubHop presets by the aircraft system.                                                                    |
| Select Preset    | Selects the preset to send when the action type is triggered.                                                                 |
| Description      | Displays the preset description from HubHop.                                                                                  |
| Show Preset Code | Shows the preset code and enables editing the code to create a custom input event.                                            |
| Preset code type | Specifies the type of custom preset, either **DataRef** or **Command**.                                                       |
| Value            | Specifies the value to send to the simulator. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |

> [!TIP]
> To enter custom code, check the **Show Preset Code** box, select the code type from the dropdown, and enter the code in the text box. There is no need to select any values from the HubHop filtering dropdowns.
