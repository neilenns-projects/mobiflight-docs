---
title: FSUIPC - Offset
description: How to use the FSUIPC - Offset input action type with MobiFlight.
aliases:
  - /guides/input-action-types/fsuipc-offset/
weight: 60
---

The **FSUIPC - Offset** action type provides a way to set simulator values via [FSUIPC](https://www.fsuipc.com/).

> [!WARNING]
> This action type is not commonly used. Use the [Microsoft Flight Simulator](/features/input-action-types/microsoft-flight-simulator/) or [X-Plane (all versions)](/features/input-action-types/x-plane-all-versions/) action type instead.

{{< screenshot image="fsuipc-offset.png" title="Screenshot of a button input with the FSUIPC - Offset action type selected." >}}

| Setting  | Description                                                                                                                       |
| -------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Type     | The type of offset, either **Int**, **Float** or **String**.                                                                      |
| Size     | The size of the value, in bytes. Either **1**, **2**, **4** or **8** for **Int** values, and **4** or **8** for **Float** values. |
| Offset   | The offset to set.                                                                                                                |
| Mask     | The mask to apply to the value before setting via FSUIPC. Useful when the same offset is used to store more than one state.       |
| BCD mode | Enables binary coded decimal mode for the value.                                                                                  |
| Value    | The value to set the offset to. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/).                   |
