---
title: WinCtrl RMP
description: Instructions on how to use the WinCtrl RMP with MobiFlight.
weight: 40
---

The WinCtrl RMP provides several output devices in MobiFlight for use when creating profiles.

## Configuring active and standby value display

Four outputs are provided to control the active and standby displays:

- `Active Value`: The current value for the **ACTIVE** (left) display.
- `Standby Value`: The current value for the **STBY/CRS** (right) display.
- `Active Mode`: Determines how the `Active Value` output is displayed.
- `Standby Mode`: Determines how the `Standby Value` output is displayed.

The supported values for `Active Mode` and `Standby Mode` are:

| Mode | Use                                  | Unit           | Simulator value -> Displayed value           |
| ---- | ------------------------------------ | -------------- | -------------------------------------------- |
| 0    | Blank display                        | not applicable | _blank_                                      |
| 1    | VHF/HF COM, VOR, and ILS frequencies | MHz            | `118.005` -> `118.005`, `113.3` -> `113.300` |
| 2    | ADF/NDB frequencies                  | KHz            | `347` -> `347.0`, `1750` -> `1750.0`         |
| 3    | Course (CRS)                         | degrees        | `240` -> `C-240`                             |
| 4    | VHF3 DATA                            | not applicable | -> `dAtA`                                    |

The value must be output in the appropriate unit for the display based on the set mode. The panel will format the value, but will not do unit conversions.

Changing the `Active Mode` or `Standby Mode` value immediately discards the stored `Active Value` or `Standby Value`. Setting the mode to `0` or `4` takes effect immediately. Setting the mode one of the other options will leave the display unchanged until a new value is provided.

## Controlling display brightness and test mode

The following outputs configure the brightness for the RMP displays:

- `Backlight Percentage`
- `LCD percentage`

Test mode for the LCD is controlled by the `LCD Test On/Off` output.

## Controlling indicator LEDs

The following outputs control the device indicator LEDs:

- `SEL`
- `VHF1`
- `VHF2`
- `VHF3`
- `LOAD`
- `HF1`
- `HF2`
- `AM`
- `NAV`
- `VOR/ILS`
- `GLS`
- `ADF`
