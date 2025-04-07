---
title: X-Plane DataRef
description: How to use the X-Plane DataRef output variable type with MobiFlight.
weight: 40
---

The **X-Plane DataRef** output variable type is the preferred way to read values from X-Plane. It provides access to over 7,000 presets from [HubHop](https://www.hubhop.com/) to interface with many popular aircraft supported by the simulator.

> [!TIP]
> To update the HubHop event list, select the **Download Latest Presets** menu item from the **Extras** > **HubHop** menu.

{{< tabs items="Default view,Custom preset code view" >}}

{{< tab >}}

{{< screenshot image="x-plane-dataref.png" title="Screenshot of an output configuration with the X-Plane DataRef output variable type selected." >}}

{{< /tab >}}

{{< tab >}}

{{< screenshot image="x-plane-dataref-show-preset-code.png" title="Screenshot of an output configuration with the X-Plane DataRef output variable type selected and the Show Preset Code checkbox checked." >}}

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

> [!TIP]
> To enter custom code, check the **Show Preset Code** box and enter the code in the text box. There is no need to select any values from the HubHop filtering dropdowns.
