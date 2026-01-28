---
title: Troubleshooting
aliases:
  - /joysticks/winwing/winwing-cdu/troubleshooting/
  - /game-controllers/winwing/winwing-cdu/troubleshooting/
weight: 80
---

## I do not want MobiFlight to take over the CDU

To prevent MobiFlight from taking over the CDU, disable it by following the [disabling game controllers](/game-controllers/disabling/) guide.

## Buttons and LEDs do not work

Button and LED support is not automatic. For each plane, a MobiFlight profile needs to be loaded. Use a [pre-made profile](/game-controllers/winwing/premade-profiles/), or [create a custom profile](/game-controllers/winctrl/custom-profiles/).

## The font on the display is misaligned or display borders are wrong

MobiFlight relies on the CDU default power-on display settings. If SimAppPro is run before MobiFlight, the display settings are modified and will result in misaligned content. To resolve the issue, close SimAppPro, then disconnect and reconnect the CDU from USB to reset the display settings to defaults.
