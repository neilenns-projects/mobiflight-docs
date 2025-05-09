---
title: WINWING devices
description: How to use WINWING devices with MobiFlight.
aliases:
  - /joysticks/winwing/
next: /game-controllers/winwing/premade-profiles/
weight: 50
---

MobiFlight supports the WINWING FCU, EFIS, MCDU and PFP 3N.

WINWING devices are automatically shown in the [input](/game-controllers/configuring-input/) and [output](/game-controllers/configuring-output/) configuration dialogs. They will not appear in the **Modules** tab of the **Settings** dialog as they are not [boards](/boards/).

The WINWING CDU requires the MobiFlight 11 beta, and its inputs work like any other [game controller input](/game-controllers/configuring-input/). The display portion of the CDU with MobiFlight requires additional configuration, and is only supported with specific aircraft. See the [WINWING CDU documentation](/game-controllers/winwing/winwing-cdu/) for more information.

> [!TIP]
> To confirm WINWING devices are seen by MobiFlight, use the **Peripherals** tab of the **Settings** dialog.

## Troubleshooting

If the WINWING device does not appear in the **Peripherals** tab of the **Settings** dialog, make sure the joystick has the latest firmware installed, and that the SIMAPP PRO application isn't running. Also, try restarting MobiFlight: devices plugged in after MobiFlight is launched are not automatically detected.
