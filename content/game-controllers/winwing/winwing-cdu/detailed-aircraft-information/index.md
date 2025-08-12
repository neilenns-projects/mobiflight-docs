---
title: Detailed aircraft information
description: Additional information regarding setup, restrictions and specialties of certain aircraft.
aliases:
  - /joysticks/winwing/winwing-cdu/detailed-aircraft-information/
weight: 50
---

Certain aircraft require additional steps for the WINWING CDU display to work properly. See the section below for the necessary steps for each aircraft.

{{% details title="FlyByWire A32NX and Headwind A339x" closed="true" %}}

The FlyByWire A32NX support requires FBW SimBridge.

Run the FlyByWire installer, select the **Aircraft** section, then the **FBW SimBridge** feature. Click **Install** to complete the installation.

{{< screenshot image="fbw-simbridge.png" title="Screenshot of the FlyByWire installer with the FBW SimBridge feature highlighted." >}}

When prompted during the installation process, toggle the **Autostart Disabled** option to the on position.

{{< screenshot image="autostart-enabled.png" title="Screenshot of the FlyByWire installer with the Autostart enabled option turned on." >}}

If autostart was disabled during installation, it can be re-enabled by selecting the **{{< icon "cog" >}} Autostart...** button in the FlyByWire installer.

{{< screenshot image="autostart-button.png" title="Screenshot of the FlyByWire installer with the Autostart... button highlighted." >}}

{{% /details %}}

{{% details title="PMDG 737 and 777" closed="true" %}}

The additional steps for PMDG aircraft happen automatically on first run in MobiFlight.

If the aircraft fails to work, enable the data communication manually by editing the file `737_Options.ini / 777_Options.ini`, located in the 737/777 persistent storage folder.

- For Microsoft Store distribution, it is located at:
  - MSFS 2020: `%LOCALAPPDATA%\Packages\Microsoft.FlightSimulator_8wekyb3d8bbwe\LocalState\packages\pmdg-aircraft-<type>\work\`.
  - MSFS 2024: `%LOCALAPPDATA%\Packages\Microsoft.Limitless_8wekyb3d8bbwe\LocalState\WASM\MSFS2024\pmdg-aircraft-<type>\work\`.
- For Steam distribution, it is located at:
  - MSFS 2020: `%APPDATA%\Microsoft Flight Simulator\Packages\pmdg-aircraft-<type>\work\`.
  - MSFS 2024: `%APPDATA%\Microsoft Flight Simulator 2024\WASM\MSFS2024\pmdg-aircraft-<type>\work\`.

`<type>` will refer to the aircraft designator. For example:

- 738
- 77w

The following lines need to be added to the bottom of the file:

```ini
[SDK]
EnableCDUBroadcast.0=1
EnableCDUBroadcast.1=1
```

{{% /details %}}
