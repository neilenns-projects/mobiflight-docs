---
title: Installing Python
description: Installing Python for use with MobiFlight.
---

Python is the external MobiFlight scripting language, e.g., needed to connect custom aircraft APIs to the WinWing CDUs.

#### Required Python environment (all three are checked by MobiFlight)

- Minimum installed Python version: `v3.10`
- Python path is set in the Windows PATH system variable.
- Installed Python packages: `websockets, gql, SimConnect`

## Installation instructions

{{% steps %}}

### Download and install Python

[Download](https://www.python.org/downloads/) and install the official Python release. Make sure to enable adding Python to the PATH during the installation process.

> [!WARNING]
> **Do not forget to set checkmark for adding python.exe to PATH**

{{< screenshot image="python-installer.png" title="Screenshot of the Python installer with the Add python.exe to PATH option enabled." >}}

### Install required Python packages

Open **Windows Terminal** or **Command Prompt**, then enter the following command:

```powershell
pip install gql simconnect websockets --upgrade
```

{{% /steps %}}
