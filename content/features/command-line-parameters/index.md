---
title: Command line parameters
description: Command line parameters to control how MobiFlight launches.
---

MobiFlight supports the following command line parameters:

| Parameter | Description                                                                                         | Example                                                           |
| --------- | --------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| `autoRun` | Enables AutoRun mode.                                                                               | `MobiFlight-Connector.exe /autoRun`                               |
| `cfg`     | Specifies the project to open on startup. If not specified, MobiFlight opens the last used project. | `MobiFlight-Connector.exe /cfg "C:\MobiFlight\Cessna 172.mfproj"` |

To load a specific project and automatically start `Run` mode when the flight simulator is detected, combine the parameters:

```powershell
MobiFlight-Connector.exe /cfg "C:\MobiFlight\Cessna 172.mfproj" /autoRun
```
