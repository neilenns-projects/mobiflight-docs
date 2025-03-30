---
title: Supported aircraft
weight: 50
---

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

## PMDG Setup

> [!NOTE]
> Necessary adaptions should happen automatically on first run.

### Information for manual setup in case of issues

To enable the data communication, the file `737_Options.ini / 777_Options.ini`, located in the 737/777 persistent storage folder, needs to extended.

- For Microsoft Store distribution, it is located at `%LOCALAPPDATA%\Packages\Microsoft.FlightSimulator_8wekyb3d8bbwe\LocalState\packages\pmdg-aircraft-737\work\`.
- For Steam distribution, it is located at `%APPDATA%\Microsoft Flight Simulator\Packages\pmdg-aircraft-737\work\`.
- For 777 the folder is called `pmdg-aircraft-77w`

The following lines need to be added to the bottom of the file:

```ini
[SDK]
EnableCDUBroadcast.0=1
EnableCDUBroadcast.1=1
```
