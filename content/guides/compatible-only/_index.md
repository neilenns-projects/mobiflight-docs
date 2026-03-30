---
title: Boards only show as compatible
description: Step-by-step guide to solving boards that only appear as compatible in MobiFlight.
---

Sometimes boards that were previously flashed with MobiFlight will only show as **Compatible** in the MobiFlight modules dialog. To resolve this, try the following.

{{% steps %}}

### Ensure other apps aren't using the COM port

Many other applications open the COM port to connected boards automatically, preventing MobiFlight from communicating with the board. Common apps causing this issue include:

- Arduino IDE
- CURA
- Joystick configuration software
- Sim Racing Studio
- WingFlex

Close any of these applications that may be running. A PC reboot may be necessary to ensure the conflicting applications are fully closed. Then, try running MobiFlight again.

If it still fails, try moving the board to a different COM port, or uninstall it using Windows Device Manager then plug it in again.

### Try removing all connected hats and devices removed

Low-quality Arduino screw terminal hats may interfere with board detection. Incorrectly connected devices can also cause shorts, preventing the board from being used. Try removing all hats and disconnecting all devices from the board, then run MobiFlight again.

### Collect logs for additional support

If the previous steps do not resolve the flashing error, start a thread in the [#MobiFlight](https://discord.com/channels/608690978081210392/1028767888242376794) support channel in [Discord](https://discord.gg/yUaBqMbz). Include the following information:

- The type of board being flashed.
- A photo of the specific board, with the chips near the USB connector clearly visible.
- The complete logs collected by following the [sharing logs guide](/guides/sharing-logs/). Set the log level to **Debug** when enabling logging.

{{% /steps %}}
