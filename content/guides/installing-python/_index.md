---
title: Installing Python
description: Installing Python for use with MobiFlight.
---

Python is the primary scripting language used by MobiFlight to connect custom aircraft APIs to [WinWing CDUs](/game-controllers/winwing/winwing-cdu/). The following must be installed for MobiFlight to work with Python:

- Python version `v3.11` or later.
- The `websockets`, `gql`, and `SimConnect` Python packages.

## Python installation instructions

{{% steps %}}

### Install from the Microsoft Store

[Install Python from the Microsoft Store](https://apps.microsoft.com/detail/9PNRBTZXMB4Z?hl=en-us&gl=US&ocid=pdpshare).

{{< screenshot image="store-python.png" title="Screenshot of the Microsoft Store listing for Python 3.13 with the Install button highlighted." >}}

### Install required Python packages

Open a **Command Prompt**:

{{< screenshot image="command-prompt.png" title="Screenshot of Windows start menu with the Command Prompt application highlighted." >}}

Then run the following command:

```powershell
pip install gql websockets simconnect --upgrade --no-warn-script-location
```

{{< screenshot image="pip-install.png" title="Screenshot of Command Prompt with the pip install command entered." >}}

> [!IMPORTANT]
> The command must be run from a **Command Prompt**, not from within Python.
>
> If the result of the command is `SyntaxError: invalid syntax`, it means it was run from within Python instead of a command prompt.

{{% /steps %}}
