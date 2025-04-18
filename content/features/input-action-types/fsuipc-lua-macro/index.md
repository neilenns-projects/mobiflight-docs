---
title: FSUIPC - Lua Macro
description: How to use the FSUIPC - Lua Macro input action type with MobiFlight.
aliases:
  - /guides/input-action-types/fsuipc-lua-macro/
weight: 90
---

The **FSUIPC - Lua Macro** action type provides a way to run a Lua script configured in [FSUIPC](https://www.fsuipc.com/).

> [!WARNING]
> This action type is not commonly used. Use the [Microsoft Flight Simulator](/features/input-action-types/microsoft-flight-simulator/) or [X-Plane (all versions)](/features/input-action-types/x-plane-all-versions/) action type instead.

{{< screenshot image="fsuipc-lua-macro.png" title="Screenshot of a button input with the FSUIPC - Lua Macro action type selected." >}}

| Setting    | Description                                                                                                     |
| ---------- | --------------------------------------------------------------------------------------------------------------- |
| Macro Name | The name of the macro to invoke.                                                                                |
| Value      | The value to send to the macro. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |
