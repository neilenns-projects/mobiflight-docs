---
title: FSUIPC Offset
description: How to use the FSUIPC Offset output variable type with MobiFlight.
weight: 30
---

The **FSUIPC Offset** output variable type provides a way to read simulator values via [FSUIPC](https://www.fsuipc.com/).

> [!WARNING]
> This variable type is not commonly used. Use [SimConnect (MSFS)](/features/output-variable-types/simconnect-msfs/) or [X-Plane (DataRef)](/features/output-variable-types/x-plane-dataref/) instead.

{{< screenshot image="fsuipc-offset.png" title="Screenshot of an output configuration the FSUIPC Offset output variable type selected." >}}

| Setting         | Description                                                                                                                       |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Use preset      | Selects a preset for common aircraft variables.                                                                                   |
| Use             | When clicked, loads the preset from the **Use preset** button.                                                                    |
| Offset          | The FSUIPC offset read.                                                                                                           |
| Value Type      | The type of offset, either **Int**, **Float** or **String**.                                                                      |
| Size in Bytes   | The size of the value, in bytes. Either **1**, **2**, **4** or **8** for **Int** values, and **4** or **8** for **Float** values. |
| Mask value with | The mask to apply to the value after reading via FSUIPC. Useful when the same offset is used to store more than one state.        |
| ...             | Opens a bit mask editor for visual editing of the mask value.                                                                     |
| BCD mode        | Enables binary coded decimal mode for the value.                                                                                  |
