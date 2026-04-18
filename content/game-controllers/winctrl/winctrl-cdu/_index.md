---
title: WinCtrl CDU
description: Instructions on how to use the WinCtrl CDU with MobiFlight.
next: /game-controllers/winctrl/winctrl-cdu/detailed-aircraft-information/
aliases:
  - /joysticks/winwing/winwing-cdu/
  - /game-controllers/winwing/winwing-cdu/
weight: 30
---

<!-- markdownlint doesn't know about ### being used inside cards, so disable the rule -->
<!-- markdownlint-disable-file MD001 -->

> [!WARNING]
> MobiFlight and SimAppPro cannot be used with a CDU at the same time. If using MobiFlight with the CDU, SimAppPro must be completely exited.

MobiFlight supports WinCtrl CDU devices. All buttons are automatically available as [game controller inputs](/game-controllers/configuring-input/); however, using the display for output requires additional setup and is only supported with the following aircraft:

<!-- The list of supported aircraft is in the winctrl-supported-aircraft.json file. Add new aircraft there -->
<!-- and they will automatically get inserted into the page here. -->

{{< winctrl-supported-aircraft >}}

To use MobiFlight with a WinCtrl CDU, take the following steps:

{{% steps %}}

### Install the latest version of MobiFlight

MobiFlight version 11 or later is required to use the WinFlex CDU.

### Configure the aircraft

Some aircraft, such as the PMDG 737 and PMDG 777, require additional configuration. See the [detailed aircraft information](/game-controllers/winctrl/winctrl-cdu/detailed-aircraft-information/) and follow the appropriate steps for the relevant airplane.

### Verify the CDU is detected

Run MobiFlight, then check the CDU display. If MobiFlight detects the CDU on startup, the CDU display will show **-->MobiFlight<--**.

{{< screenshot image="cdu-display.png" title="Photo of a WinCtrl CDU with -->MobiFlight<-- showing on the display." >}}

{{% /steps %}}

## Tips

Do not run SimAppPro at the same time as MobiFlight.

MobiFlight relies on the CDU default power-on display settings. If SimAppPro is run before MobiFlight, the display settings are modified and will result in misaligned content. To resolve the issue, close SimAppPro, then disconnect and reconnect the CDU from USB to reset the display settings to defaults.

If multiple CDUs are connected, they need to be assigned separate modes. Use SimAppPro to set each CDU to CAPTAIN, OBSERVER or CO-PILOT mode.

Only **default font** is supported.
