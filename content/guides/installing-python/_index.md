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

> [!WARNING] > **Do not forget to set checkmark for adding python.exe to PATH**

{{< screenshot image="python-installer.png" title="Screenshot of the Python installer with the Add python.exe to PATH option enabled." >}}

### Install required Python packages

Open **Windows Terminal** or **Command Prompt**, then enter the following command:

```powershell
pip install gql simconnect websockets --upgrade
```

{{< screenshot image="pip-install.png" title="Screenshot of Windows Terminal with the pip install command entered." >}}

{{% /steps %}}

## Troubleshooting

If MobiFlight fails to find Python after completing the installation steps above, it is typically caused by multiple versions of Python installed at the same time.

To resolve the issue:

{{% steps %}}

### Open the app execution aliases dialog

From the **Start** menu, type **app execution**, and select the **Manage app execution aliases** entry.

{{< screenshot image="start-menu-app-execution.png" title="Screenshot of the Windows Start menu with the Manage app execution aliases entry highlighted." >}}

### Turn off the python.exe alias

In the list of app aliases, look for entries associated with **python.exe** and set the toggle switch to **Off**

{{< screenshot image="python-off.png" title="Screenshot of the Manage app execution aliases settings with the python.exe entry turned off." >}}

{{% /steps %}}
