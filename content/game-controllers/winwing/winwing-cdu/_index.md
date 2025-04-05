---
title: WINWING CDU
description: Instructions on how to use the WINWING CDU with MobiFlight.
next: /game-controllers/winwing/winwing-cdu/detailed-aircraft-information/
aliases:
  - /joysticks/winwing/winwing-cdu/
weight: 30
---

MobiFlight supports WINWING CDU devices in the most recent beta build. The keys are automatically available as [game controller inputs](/game-controllers/configuring-input/); however, using the display for output requires additional setup and is only supported with the following aircraft:

| Platform | Aircraft    | Supported configurations | Comment                                                                                                   |
| -------- | ----------- | ------------------------ | --------------------------------------------------------------------------------------------------------- |
| MSFS     | Fenix A3xx  | CPT or FO or CPT+FO      |                                                                                                           |
| MSFS     | FSLabs A321 | CPT                      |                                                                                                           |
| MSFS     | PMDG 737    | CPT or FO or CPT+FO      | [Requires additional configuration](/game-controllers/winwing/winwing-cdu/detailed-aircraft-information/) |
| MSFS     | PMDG 777    | CPT or FO or CPT+FO      | [Requires additional configuration](/game-controllers/winwing/winwing-cdu/detailed-aircraft-information/) |
| MSFS     | iFly 737    | CPT or FO or CPT+FO      | CPT+FO untested so far                                                                                    |
| MSFS     | TFDi MD-11  | CPT or FO or CPT+FO      |                                                                                                           |

To get the beta build and install pre-requisites for CDU display support, take the following steps:

{{% steps %}}

### Install the beta build

Opt in to MobiFlight beta builds by selecting **Settings** from the **Extras** menu, then checking the **Yes, I would like to receive beta version updates** option. Click **OK** to close the dialog, then restart MobiFlight. The app will prompt to download and install the latest beta.

{{< screenshot image="beta-opt-in.png" title="Screenshot of the Settings dialog with the Yes, I would like to receive beta version updates option checked." >}}

### Install Python

CDU support in MobiFlight requires Python and additional support libraries. Follow the [Python installation guide](/guides/installing-python/) to install the necessary components, then restart MobiFlight.

### Configure the aircraft

Some aircraft, such as the PMDG 737 and PMDG 777, require additional configuration. See the [detailed aircraft information](/game-controllers/winwing/winwing-cdu/detailed-aircraft-information/) and follow the appropriate steps for the relevant airplane.

### Verify the CDU is detected

Run MobiFlight, then check the CDU display. If MobiFlight detects the CDU on startup, the CDU display will show **-->MobiFlight<--**.

{{< screenshot image="cdu-display.png" title="Photo of a WINWING CDU with -->MobiFlight<-- showing on the display." >}}

{{% /steps %}}

## Tips

Do not run SimAppPro at the same time as MobiFlight.

MobiFlight relies on the CDU default power-on display settings. If SimAppPro is run before MobiFlight, the display settings are modified and will result in misaligned content. To resolve the issue, close SimAppPro, then disconnect and reconnect the CDU from USB to reset the display settings to defaults.

If multiple CDUs are connected, they need to be assigned separate modes. Use SimAppPro to set each CDU to CAPTAIN, OBSERVER or CO-PILOT mode.

Only **default font** is supported.
