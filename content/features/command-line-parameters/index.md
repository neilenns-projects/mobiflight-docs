---
title: Command line parameters
description: Command line parameters to control how MobiFlight launches.
---

MobiFlight supports the following command line parameters:

| Parameter | Description                                                                                                               | Example                                                    |
| --------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| `autoRun` | Enables AutoRun mode.                                                                                                     | `MobiFlight-Connector.exe /autoRun`                        |
| `cfg`     | Specifies the configuration file to open on startup. If not specified, MobiFlight opens the last used configuration file. | `MobiFlight-Connector.exe /cfg "C:\MobiFlight\config.mcc"` |

To load a specific configuration file and automatically start `Run` mode when the flight simulator is detected, combine the parameters:

```powershell
MobiFlight-Connector.exe /cfg "C:\MobiFlight\myconfig.mcc" /autoRun
```
