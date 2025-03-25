---
title: FSUIPC - Offset
description: How to use the FSUIPC - Offset input action type with MobiFlight.
weight: 60
---

The **FSUIPC - Offset** action type provides a way to set simulator values via [FSUIPC](https://www.fsuipc.com/).

> [!WARNING]
> This action type is not commonly used. Use the [Microsoft Flight Simulator](/guides/input-action-types/microsoft-flight-simulator/) or [X-Plane (all versions)](/guides/input-action-types/x-plane-all-versions/) action type instead.

{{< screenshot image="fsuipc-offset.png" title="Screenshot of a button input with the FSUIPC - Offset action type selected." >}}

| Setting         | Description                                                                                                                       |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Use preset      | Selects a preset for common aircraft variables.                                                                                   |
| Use             | When clicked, loads the preset from the **Use preset** dropdown.                                                                  |
| Offset          | The FSUIPC offset to set.                                                                                                         |
| Value Type      | The type of offset, either **Int**, **Float** or **String**                                                                       |
| Size in Bytes   | The size of the value, in bytes. Either **1**, **2**, **4** or **8** for **Int** values, and **4** or **8** for **Float** values. |
| Mask value with | The mask to apply to the value before setting via FSUIPC. Useful when the same offset is used to store more than one state.       |
| ...             | Opens a bit mask editor for visual editing of the mask value.                                                                     |
| BCD mode        | Enables binary coded decimal mode for the value.                                                                                  |
| Set Value       | The value to set the offset to. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/).                   |
