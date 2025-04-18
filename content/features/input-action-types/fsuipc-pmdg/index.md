---
title: FSUIPC - PMDG - Event ID
description: How to use the FSUIPC - PMDG - Event ID input action type with MobiFlight.
aliases:
  - /guides/input-action-types/fsuipc-pmdg/
weight: 80
---

The **FSUIPC - PMDG - Event ID** action type provides a way to set values in PMDG aircraft that are inaccessible via the [Microsoft Flight Simulator](/features/input-action-types/microsoft-flight-simulator/) or [X-Plane (all versions)](/features/input-action-types/x-plane-all-versions/) action type.

> [!WARNING]
> This action type is only for controlling specific events in PMDG aircraft that are inaccessible using other action types.

{{< screenshot image="fsuipc-pmdg.png" title="Screenshot of a button input with the FSUIPC - PMDG - Event ID action type selected." >}}

| Setting      | Description                                                                                                            |
| ------------ | ---------------------------------------------------------------------------------------------------------------------- |
| Aircraft     | Selects the PMDG aircraft type, either **B737**, **B777** or **B747**.                                                 |
| Use preset   | Selects a preset for the specified aircraft.                                                                           |
| Use          | When clicked, loads the preset from the **Use preset** dropdown.                                                       |
| Event ID     | The Event ID to invoke.                                                                                                |
| Mouse Param  | The mouse event to invoke.                                                                                             |
| Custom Param | The parameter to send to the Event ID. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |
