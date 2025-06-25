---
title: WINWING devices
description: How to use WINWING devices with MobiFlight.
aliases:
  - /joysticks/winwing/
next: /game-controllers/winwing/premade-profiles/
weight: 50
---

<!-- Markdownlint doesn't know about consecutive GitHub tip blocks -->
<!-- markdownlint-disable MD028-->

MobiFlight supports the WINWING FCU, EFIS, MCDU, PAP 3, PFP 3N and PFP 7.

The WINWING CDU requires the MobiFlight 11 beta, and its inputs work like any other [game controller input](/game-controllers/configuring-input/). The display portion of the CDU with MobiFlight requires additional configuration, and is only supported with specific aircraft. See the [WINWING CDU documentation](/game-controllers/winwing/winwing-cdu/) for more information.

WINWING devices are automatically shown in the [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configuration dialogs. They will not appear in the **Modules** tab of the **Settings** dialog as they are not [boards](/boards/).

> [!TIP]
> Many pre-made MobiFlight profiles for WINWING devices are available. See [flightsim.to](https://flightsim.to/discover/winwing) for Microsoft Flight Simulator profiles, and the [X-Plane forums](https://forums.x-plane.org/index.php?/search/&q=winwing&quick=1) for X-Plane profiles. After downloading a profile, see the [Using pre-made MobiFlight profiles](/game-controllers/winwing/premade-profiles/) page for instructions on how to use them.
>
> If no pre-made profile is available, make a custom one using [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configurations.

## Troubleshooting

> [!TIP]
> To confirm WINWING devices are seen by MobiFlight, use the **Peripherals** tab of the **Settings** dialog.

If the WINWING device does not appear in the **Peripherals** tab of the **Settings** dialog, make sure the joystick has the latest firmware installed, and that the SIMAPP PRO application isn't running. Also, try restarting MobiFlight: devices plugged in after MobiFlight is launched are not automatically detected.
