---
title: SimConnect (MSFS)
description: How to use the SimConnect (MSFS) output variable type with MobiFlight.
weight: 10
---

The **SimConnect (MSFS)** output variable type is the preferred way to read values from Microsoft Flight Simulator 2020 and 2024. It provides access to over 20,000 presets from [HubHop](https://www.hubhop.com/) to interface with nearly every aircraft supported by the simulator.

> [!TIP]
> To update the HubHop event list, select the **Download Latest Presets** menu item from the **Extras** > **HubHop** menu.

{{< tabs items="Default view,Custom preset code view" >}}

{{< tab >}}

{{< screenshot image="simconnect-msfs-default.png" title="Screenshot of an output configuration with the SimConnect (MSFS) output variable type selected." >}}

{{< /tab >}}

{{< tab >}}

{{< screenshot image="simconnect-msfs-show-preset-code.png" title="Screenshot of an output configuration with the SimConnect (MSFS) output variable type selected and the Show Preset Code checkbox checked." >}}

{{< /tab >}}

{{< /tabs >}}

| Setting          | Description                                                                                      |
| ---------------- | ------------------------------------------------------------------------------------------------ |
| Search           | Provides text filtering of the HubHop presets.                                                   |
| Vendor           | Filters the list of HubHop presets by the aircraft vendor.                                       |
| Aircraft         | Filters the list of HubHop presets by the aircraft name.                                         |
| System           | Filters the list of HubHop presets by the aircraft system.                                       |
| Select Preset    | Selects the preset to use when reading the value from the simulator.                             |
| Description      | Displays the preset description from HubHop.                                                     |
| Show Preset Code | Shows the preset code and enables editing the code to create a custom script to read a variable. |
| +                | Expands the preset code text box to enable multi-line editing.                                   |

> [!TIP]
> To enter custom code, check the **Show Preset Code** box and enter the code in the preset code text box. There is no need to select any values from the HubHop filtering dropdowns.
