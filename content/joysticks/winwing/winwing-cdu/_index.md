---
title: WINWING CDU
description: Instructions on how to use the WINWING CDU with MobiFlight.
weight: 30
---

WINWING CDU display support is automatic on run, if a supported plane and a CDU are detected. To prevent MobiFlight from taking over the CDU, disable it by following the [disabling joysticks](/joysticks/disabling/) guide.

## Installing Python

> [!IMPORTANT]
> WINWING CDU support depends on Python. See the [Python installation guide](/guides/installing-python/) for steps on how to install Python for use with MobiFlight.

## General remarks

- If MobiFlight has detected the CDU on startup, it will show `->MobiFlight<-` on the display.
- Do not run SimAppPro in parallel. After using SimAppPro, reconnect device to the USB port. MobiFlight currently relies on the CDU default power-on display settings, which might have been changed by a running  SimAppPro instance.
- If multiple CDUs are connected, they need to be assigned separate modes. Use SimAppPro to set each CDU to CAPTAIN, OBSERVER or CO-PILOT mode.
- Only **default font** is supported.

## Further information

{{< cards >}}

{{< card link="/joysticks/winwing/winwing-cdu/troubleshooting/" title="Troubleshooting" icon="information" >}}
{{< card link="/joysticks/winwing/#winwwing-cdu-supported-aircraft" title="Supported aircraft" icon="information" >}}
{{< card link="/joysticks/winwing/winwwing-cdu/detailed-aircraft-information" title="Detailed aircraft information" icon="information" >}}
{{< card link="/joysticks/winwing/winwing-cdu/dev-instructions/" title="Developer instructions" icon="information" >}}

{{< /cards >}}
