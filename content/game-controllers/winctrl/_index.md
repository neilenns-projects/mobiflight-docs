---
title: WinCtrl devices
description: How to use WinCtrl devices with MobiFlight.
aliases:
  - /joysticks/winwing/
  - /game-controllers/winwing/
next: /game-controllers/winctrl/winctrl-cdu/
weight: 50
---

<!-- Markdownlint doesn't know about consecutive GitHub tip blocks -->
<!-- markdownlint-disable MD028-->

MobiFlight supports the WinCtrl AGP, ECAM, EFIS, FCU, MCDU, PAP 3, PFP 3N, PFP 4, PFP 7, 3N PDC, 3M PDC, PTO 2, TCAS, Airbus throttle, and Airbus sidestick.

The WinCtrl CDU inputs work like any other [game controller input](/game-controllers/configuring-input/). The display portion of the CDU with MobiFlight requires additional configuration, and is only supported with specific aircraft. See the [WinCtrl CDU documentation](/game-controllers/winctrl/winctrl-cdu/) for more information.

WinCtrl devices are automatically shown in the [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configuration dialogs. They will not appear in the **Modules** tab of the **Settings** dialog as they are not [boards](/boards/).

> [!TIP]
> Many MobiFlight profiles for WinCtrl devices are available from the community. See [flightsim.to](https://flightsim.to/miscellaneous/mobiflight-profiles) for Microsoft Flight Simulator profiles, and the [X-Plane forums](https://forums.x-plane.org/index.php?/search/&q=winwing&quick=1) for X-Plane profiles. After downloading a profile, see the [Using community MobiFlight profiles](/guides/using-community-profiles/) page for instructions on how to use them.

## Troubleshooting

If the WinCtrl device does not appear in the **Peripherals** tab of the **Settings** dialog, make sure the joystick has the latest firmware installed, and that the SIMAPP PRO application isn't running. Also, try restarting MobiFlight: devices plugged in after MobiFlight is launched are not automatically detected.

> [!TIP]
> To confirm WinCtrl devices are seen by MobiFlight, use the **Peripherals** tab of the **Settings** dialog.
