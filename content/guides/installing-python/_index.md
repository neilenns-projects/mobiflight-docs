---
title: Installing Python
description: Installing Python for use with MobiFlight.
---

<!-- markdownlint can't handle consecutive GitHub-style callouts. -->
<!-- markdownlint-disable MD028 -->

Python is the primary scripting language used by MobiFlight to connect custom aircraft APIs to [WinWing CDUs](/game-controllers/winwing/winwing-cdu/). The following must be installed for MobiFlight to work with Python:

- Python version `v3.11` or later.
- The `websockets`, `gql`, and `SimConnect` Python packages.

## Python installation instructions

{{% steps %}}

### Install from the Microsoft Store

[Install Python from the Microsoft Store](ms-windows-store://pdp/?productid=9PNRBTZXMB4Z).

{{< screenshot image="store-python.png" title="Screenshot of the Microsoft Store listing for Python 3.13 with the Install button highlighted." >}}

### Install required Python packages

Open a **Command Prompt**:

{{< screenshot image="command-prompt.png" title="Screenshot of Windows start menu with the Command Prompt application highlighted." >}}

Then run the following command:

```powershell
python -m pip install gql websockets simconnect --upgrade --no-warn-script-location
```

{{< screenshot image="pip-install.png" title="Screenshot of Command Prompt with the pip install command entered." >}}

> [!IMPORTANT]
> The command must be run from a **Command Prompt**, not from within Python.
>
> If the result of the command is `SyntaxError: invalid syntax`, it means it was run from within Python instead of a command prompt.

> [!TIP]
> If `pip` gives a warning about adding directories to PATH, you can safely ignore it.

{{% /steps %}}
