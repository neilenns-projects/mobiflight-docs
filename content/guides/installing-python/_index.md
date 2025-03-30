---
title: Installing Python
---

Python is the external MobiFlight scripting language, e.g. needed to connect custom aircraft APIs to the WinWing CDUs.

**Required Python environment (all three are checked by MobiFlight):**

- Minimum installed Python version: `v3.10`
- Python path is set in the windows PATH system variable.
- Installed Python packages: `websockets, gql, SimConnect`

## Installation instructions

{{% steps %}}

### [Download](https://www.python.org/downloads/) and install Python

> [!WARNING]
> **Do not forget to set checkmark for adding python.exe to PATH**

{{< screenshot image="python-installer.png" title="Python installer." >}}

### Install the following Python packages via command line

(It does not matter in which folder you are, just execute on the command line.)

```text
pip install websockets gql simconnect
```

List and check all installed packages and versions with:

```text
pip freeze
```

Minimum required version for websockets is v14.0. If list shows lower version, update with:

```text
pip install websockets --upgrade
```

{{% /steps %}}
