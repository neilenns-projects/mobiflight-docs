---
title: Solving flashing errors
description: Step-by-step guide to solving errors when flashing supported MobiFlight boards.
ogimage: screenshots/flashing-error.png
---

When connecting a new board, MobiFlight prompts to install the software on the board to make it work with MobiFlight. In some cases, that installation fails and MobiFlight will display an error dialog.

{{< screenshot image="flashing-error.png" title="Screenshot of the flashing failed error dialog." >}}

Use the following steps to troubleshoot the issue.

{{% steps %}}

### Verify the board is supported

Check the [recommended and supported boards](/boards/) and confirm the board is supported by MobiFlight. Many unsupported boards have similar names to supported boards and will not work. For example, the Pro Micro (8MHz) is not supported but the Pro Micro (16MHz) is.

### Install required drivers

Some boards require additional driver installation before they can be used with MobiFlight. For example, boards with counterfeit CH340G serial communication chips will fail to flash unless the correct driver is installed. Follow the [installing drivers guide](/guides/installing-drivers/) to determine the type of serial communication chip used by your board, then install the correct drivers if necessary.

### Ensure other apps aren't using the COM port

Many other applications open the COM port to connected boards automatically, preventing MobiFlight from communicating with the board. Common apps with this issue include:

- CURA
- Arduino IDE
- Joystick configuration software

Close any of these applications that may be running. A PC reboot may be necessary to ensure the conflicting applications are fully closed. Then, try flashing the board again.

### Collect logs for additional support

If the previous steps do not resolve the flashing error, start a thread in the [#MobiFlight](https://discord.com/channels/608690978081210392/1028767888242376794) support channel in [Discord](https://discord.gg/yUaBqMbz). Include the following information:

- The type of board being flashed.
- A photo of the specific board, with the chips near the USB connector clearly visible.
- The complete logs collected by following the [sharing logs guide](/guides/sharing-logs/). Set the log level to **Debug** when enabling logging.

{{% /steps %}}
