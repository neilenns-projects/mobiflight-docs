---
title: FSUIPC - Event ID
description: How to use the FSUIPC - Event ID input action type with MobiFlight.
weight: 70
---

The **FSUIPC - Event ID** action type provides a way to trigger SimConnect events via [FSUIPC](https://www.fsuipc.com/).

> [!WARNING]
> This action type is not commonly used. Use the [Microsoft Flight Simulator](/guides/input-action-types/microsoft-flight-simulator/) or [X-Plane (all versions)](/guides/input-action-types/x-plane-all-versions/) action type instead.

{{< screenshot image="fsuipc-event-id.png" title="Screenshot of a button input with the FSUIPC - Event ID action type selected." >}}

| Setting    | Description                                                                                                            |
| ---------- | ---------------------------------------------------------------------------------------------------------------------- |
| Use preset | Selects a preset for common aircraft variables.                                                                        |
| Use        | When clicked, loads the preset from the **Use preset** dropdown.                                                       |
| Event ID   | The Event ID to invoke.                                                                                                |
| Para       | The parameter to send to the EVent ID. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |
