---
title: WINWING CDU
weight: 50
---

WINWING CDU display support is automatic on run, if a supported plane and a CDU are detected. To prevent MobiFlight from taking over the CDU, disable it in `Extras->Settings->Peripherals`.

## Installing Python

Follow the [guide](/guides/installing-python/).

## General remarks

- Python is a mandatory prerequisite.
- If MobiFlight has detected the CDU on startup, it will show `->MobiFlight<-` on the display.
- Do not run SimAppPro in parallel. After using SimAppPro, reconnect device to the USB port. MobiFlight currently relies on the CDU default power-on display settings, which might have been changed by a running  SimAppPro instance.
- Currently, only **default font** is supported.
- Use SimAppPro to set the CDU to CAPTAIN, OBSERVER or CO-PILOT mode. If several CDUs are connected, they need to be in different modes.

## Further information

{{< cards >}}

{{< card link="/joysticks/winwing/winwing-cdu/troubleshooting/" title="Troubleshooting" icon="information" >}}
{{< card link="/joysticks/winwing/winwing-cdu/supported-aircraft/" title="Supported aircraft" icon="information" >}}
{{< card link="/joysticks/winwing/winwing-cdu/dev-instructions/" title="Developer instructions" icon="information" >}}

{{< /cards >}}
