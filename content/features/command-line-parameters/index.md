---
title: Command line parameters
description: Command line parameters to control how MobiFlight launches.
---

MobiFlight supports the following command line parameters:

| Parameter | Description                                                                                                               | Example                                                    |
| --------- | ------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| autoRun   | Enables AutoRun mode.                                                                                                     | `MobiFlight-Connector.exe /autoRun`                        |
| cfg       | Specifies the configuration file to open on startup. If not specified, MobiFlight opens the last used configuration file. | `MobiFlight-Connector.exe /cfg "C:\MobiFlight\config.mcc"` |

You can combine both parameters to load a specific configuration file, and automatically have MobiFlight start "Run" mode as soon as the flight sim is detected, by combining the parameters:

```powershell
MobiFlight-Connector.exe /cfg "C:\MobiFlight\myconfig.mcc" /autoRun
```
