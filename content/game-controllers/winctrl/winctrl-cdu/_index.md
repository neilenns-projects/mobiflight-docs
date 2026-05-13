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

MobiFlight supports WinCtrl CDU devices. All buttons are automatically available as [game controller inputs](/game-controllers/configuring-input/); however, using the display for output requires additional configuration specific to each aircraft. This page covers the setup process and lists all supported aircraft and their configurations.

## Supported aircraft

{{< winctrl-cdu-aircraft-table >}}

## Setup instructions

To use MobiFlight with a WinCtrl CDU, take the following steps:

{{% steps %}}

### Install the latest version of MobiFlight

MobiFlight version 11 or later is required to use the WinCtrl CDU.

### Configure the aircraft

Some aircraft, such as the PMDG 737 and PMDG 777, require additional configuration. See the [detailed aircraft information](/game-controllers/winctrl/winctrl-cdu/detailed-aircraft-information/) for your aircraft.

### Verify the CDU is detected

Run MobiFlight, then check the CDU display. If MobiFlight detects the CDU on startup, the CDU display will show **-->MobiFlight<--**.

{{< screenshot image="cdu-display.png" title="Photo of a WinCtrl CDU with -->MobiFlight<-- showing on the display." >}}

{{% /steps %}}

## Tips

- Do not run SimAppPro at the same time as MobiFlight.
- MobiFlight relies on the CDU default power-on display settings. If SimAppPro is run before MobiFlight, the display settings are modified and will result in misaligned content. To resolve the issue, close MobiFlight and power-cycle the CDU before launching MobiFlight again.
- If multiple CDUs are connected, they need to be assigned separate modes. Use SimAppPro to set each CDU to **CAPTAIN**, **OBSERVER**, or **CO-PILOT** mode.
- Only **default font** is supported.
