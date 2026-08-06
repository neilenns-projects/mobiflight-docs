---
title: Solving compatible-only boards
description: Step-by-step guide to solving boards that only appear as compatible in MobiFlight.
---

Sometimes boards that were previously flashed with MobiFlight will only show as **Compatible** in the MobiFlight modules dialog. To resolve this, try the following.

{{% steps %}}

### Ensure other apps aren't using the COM port

Many other applications open the COM port to connected boards automatically, preventing MobiFlight from communicating with the board. Common apps causing this issue include:

- Arduino IDE
- CURA
- Joystick configuration software
- RGB light controllers (e.g. iCUE, Signal RGB)
- RowsfireApp
- Sim Racing Studio
- WingFlex

Close any of these applications that may be running. A PC reboot may be necessary to ensure the conflicting applications are fully closed. Then, try running MobiFlight again.

If it still fails, try moving the board to a different COM port, or uninstall it using Windows Device Manager then plug it in again.

### Try removing all connected hats and devices

Low-quality Arduino screw terminal hats may interfere with board detection. Incorrectly connected devices can also cause shorts, preventing the board from being used. Try removing all hats and disconnecting all devices from the board, then run MobiFlight again.

### Remove devices connected to pins D0 and D1

The Arduino [Nano](/boards/recommended/arduino-nano/), [Mega 2560](/boards/supported/arduino-mega-2560/), [Mega 2560 Pro Mini](/boards/recommended/mega-2560-pro-mini/) and [Uno](/boards/supported/arduino-uno/) use pins **D0** and **D1** internally for communication with the desktop. Connecting devices to these pins can lead to connection issues. Try removing any devices connected to pins D0 and D1, then flash again.

### Collect logs for additional support

If the previous steps do not resolve the flashing error, start a thread in the [#MobiFlight](https://discord.com/channels/608690978081210392/1028767888242376794) support channel in [Discord](https://discord.gg/yUaBqMbz). Include the following information:

- The type of board being flashed.
- A photo of the specific board, with the chips near the USB connector clearly visible.
- The complete logs collected by following the [sharing logs guide](/guides/sharing-logs/). Set the log level to **Debug** when enabling logging.

{{% /steps %}}
