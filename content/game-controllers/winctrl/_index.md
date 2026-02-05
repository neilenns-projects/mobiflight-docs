---
title: WinCtrl devices
description: How to use WinCtrl devices with MobiFlight.
aliases:
  - /joysticks/winwing/
  - /game-controllers/winwing/
next: /game-controllers/winctrl/premade-profiles/
weight: 50
---

<!-- Markdownlint doesn't know about consecutive GitHub tip blocks -->
<!-- markdownlint-disable MD028-->

MobiFlight supports the WinCtrl AGP, ECAM, EFIS, FCU, MCDU, PAP 3, PFP 3N, PFP 4, PFP 7, 3N PDC, 3M PDC, PTO 2, Airbus throttle, and Airbus sidestick.

> [!NOTE]
> The clock on the AGP is not supported.

The WinCtrl CDU requires the MobiFlight 11 beta, and its inputs work like any other [game controller input](/game-controllers/configuring-input/). The display portion of the CDU with MobiFlight requires additional configuration, and is only supported with specific aircraft. See the [WinCtrl CDU documentation](/game-controllers/winctrl/winctrl-cdu/) for more information.

WinCtrl devices are automatically shown in the [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configuration dialogs. They will not appear in the **Modules** tab of the **Settings** dialog as they are not [boards](/boards/).

> [!TIP]
> Many pre-made MobiFlight profiles for WinCtrl devices are available. See [flightsim.to](https://flightsim.to/discover/winwing) for Microsoft Flight Simulator profiles, and the [X-Plane forums](https://forums.x-plane.org/index.php?/search/&q=winwing&quick=1) for X-Plane profiles. After downloading a profile, see the [Using pre-made MobiFlight profiles](/game-controllers/winctrl/premade-profiles/) page for instructions on how to use them.
>
> If no pre-made profile is available, make a custom one using [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configurations.

## Troubleshooting

> [!TIP]
> To confirm WinCtrl devices are seen by MobiFlight, use the **Peripherals** tab of the **Settings** dialog.

If the WinCtrl device does not appear in the **Peripherals** tab of the **Settings** dialog, make sure the joystick has the latest firmware installed, and that the SIMAPP PRO application isn't running. Also, try restarting MobiFlight: devices plugged in after MobiFlight is launched are not automatically detected.
