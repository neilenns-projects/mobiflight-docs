---
title: Installing Python
description: Installing Python for use with MobiFlight.
---

Python is the external MobiFlight scripting language, e.g., needed to connect custom aircraft APIs to the WinWing CDUs.

#### Required Python environment (all three are checked by MobiFlight)

- Minimum installed Python version: `v3.10`
- Installed Python packages: `websockets, gql, SimConnect`

## Installation instructions

{{% steps %}}

### Install Python

[Install Python from the Microsoft Store](https://apps.microsoft.com/detail/9PNRBTZXMB4Z?hl=en-us&gl=US&ocid=pdpshare).

{{< screenshot image="store-python.png" title="Screenshot of the Microsoft Store listing for Python 3.13 with the Install button highlighted." >}}

### Install required Python packages

Open **Windows Terminal** or **Command Prompt**, then run the following command:

```powershell
pip install gql websockets simconnect --upgrade --no-warn-script-location
```

{{< screenshot image="pip-install.png" title="Screenshot of Windows Terminal with the pip install command entered." >}}

{{% /steps %}}
