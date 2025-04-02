---
title: WINWING devices
description: How to use WINWING devices with MobiFlight.
weight: 50
---

MobiFlight supports the WINWING FCU, MCDU, and PFP3N.

> [!TIP]
> WINWING devices are automatically shown in the input and output configuration dialogs. They will not appear in the **Modules** tab of the **Settings** dialog as they are not [boards](/boards/), to confirm the WINWING device is seen by MobiFlight, use the **Peripherals** tab of the **Settings** dialog.

## WINWING CDU supported aircraft

| Platform | Aircraft    | Supported configurations | Comment                     |
|----------|-------------|--------------------------|-----------------------------|
| MSFS     | Fenix A3xx  | CPT or FO or CPT+FO      |                             |
| MSFS     | FSLabs A321 | CPT                      |                             |
| MSFS     | PMDG 737    | CPT or FO or CPT+FO      |                             |
| MSFS     | PMDG 777    | CPT or FO or CPT+FO      |                             |
| MSFS     | iFly 737    | CPT or FO or CPT+FO      | CPT+FO untested so far      |
| MSFS     | TFDi MD-11  | CPT or FO or CPT+FO      |                             |

### Work in progress

- First X-Plane 12 support
- First X-Plane 11 support
- FlyByWire A320 stable support
- Aerosoft CRJ support
- WT21 (e.g. CJ4) support

## Troubleshooting

If the WINWING device does not appear in the **Peripherals** tab of the **Settings** dialog, make sure the joystick has the latest firmware installed, and that the SIMAPP PRO application isn't running. Also, try restarting MobiFlight: devices plugged in after MobiFlight is launched are not automatically detected.
