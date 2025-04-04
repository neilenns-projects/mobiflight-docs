---
title: Troubleshooting
weight: 30
---

## I do not want MobiFlight to take over the CDU

To prevent MobiFlight from taking over the CDU, disable it by following the [disabling joysticks](/joysticks/disabling/) guide.

## A Python message keeps popping up

Install Python and needed packages exactly as described in the [guide](/guides/installing-python/). Or if no MobiFlight support is needed, disable the CDU by following the [disabling joysticks](/joysticks/disabling/) guide.

## Buttons and LEDs do not work

Button and LED support is not automatic. For each plane, a MobiFlight profile needs to be loaded. Use a [pre-made profile](/joysticks/winwing/premade-profiles/), or [create a custom profile](/joysticks/winwing/custom-profiles/).

## The font on the display is misaligned or display borders are wrong

Do not run SimAppPro in parallel. After using SimAppPro, reconnect the CDU to the USB port. MobiFlight currently relies on the CDU default power-on display settings, which might have been changed by a running SimAppPro instance.
