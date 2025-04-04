---
title: Detailed aircraft information
description: Additional information regarding setup, restrictions and specialties of certain aircraft.
weight: 50
---

{{% details title="PMDG 737 and 777" closed="true" %}}

### PMDG Setup

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

{{% /details %}}
