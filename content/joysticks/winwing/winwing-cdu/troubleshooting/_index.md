---
title: Troubleshooting
weight: 30
---

#### I do not want MobiFlight to take over the CDU

Disable it in `Extras->Settings->Peripherals`.

#### A Python message keeps popping up

Install Python and needed packages exactly as described in the [guide](/guides/installing-python/). Or if no MobiFlight support is needed, disable the CDU in `Extras->Settings->Peripherals`.

#### Plane xy does not work

See the list of currently [supported aircraft](/joysticks/winwing/winwing-cdu/supported-aircraft/) and remarks to the planes.

#### Buttons and LEDs do not work

Button and LED support is not automatic. For each plane a MobiFlight profile needs to be loaded. See [using pre-made profiles](/joysticks/winwing/premade-profiles/) or [create custom profiles](/joysticks/winwing/custom-profiles/)

#### The font on the display is misaligned or display borders are wrong

Do not run SimAppPro in parallel. After using SimAppPro reconnect the CDU to the USB port. MobiFlight currently relies on the CDU default power-on display settings, which might have been changed by a running SimAppPro instance.
