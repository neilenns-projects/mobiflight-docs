---
title: Solving WASM module disconnects
description: Troubleshooting a constantly disconnecting WASM module caused by noisy inputs.
weight: 10
---

The WASM module can disconnect repeatedly when an input is sending a continuous stream of updates to MobiFlight, even when the input is not being touched. This is most commonly caused by:

- A noisy potentiometer connected to an Arduino board.
- An uncalibrated game controller input, like the centering potentiometer in a WinCtrl EFIS or the photosensors in a WinCtrl autopilot panel.

## Identifying the noisy input

Enabling logging and watching the log output makes it easy to spot an input that is sending continuous updates.

{{% steps %}}

### Enable info logging

Follow the [logging guide](/guides/sharing-logs/) to enable **Info** logging.

### Watch for unexpected input events

Without touching any inputs, watch the log for entries showing input values changing on their own. A noisy input will produce a steady stream of log entries even when nothing is being moved.

### Identify the device

Note the board or game controller name and device listed in the log entries. This is the noisy input that needs to be addressed. In the following example, both **Light Sensor 1** and **Light Sensor 2** on the WinCtrl PFP game controller are causing the issue.

```text
04/09/2026 12:41:14(963): WINCTRL 4 PFP CAPTAIN => Light Sensor 2 => CHANGE => 5024
04/09/2026 12:41:15(57): WINCTRL 4 PFP CAPTAIN => Light Sensor 2 => CHANGE => 5056
04/09/2026 12:41:15(151): WINCTRL 4 PFP CAPTAIN => Light Sensor 1 => CHANGE => 4416
04/09/2026 12:41:15(584): WINCTRL 4 PFP CAPTAIN => Light Sensor 2 => CHANGE => 5040
04/09/2026 12:41:15(647): WINCTRL 4 PFP CAPTAIN => Light Sensor 1 => CHANGE => 4400
04/09/2026 12:41:15(677): WINCTRL 4 PFP CAPTAIN => Light Sensor 2 => CHANGE => 5008
04/09/2026 12:41:15(771): WINCTRL 4 PFP CAPTAIN => Light Sensor 2 => CHANGE => 4976
```

{{% /steps %}}

## Reducing noise from Arduino potentiometers

For potentiometers connected to Arduino boards, reduce the **Sensitivity** setting in MobiFlight and, if necessary, make hardware improvements.

{{% steps %}}

### Reduce the sensitivity setting

Open the [**Modules** dialog](/devices/potentiometer/settings-reference/#modules-dialog) for the board and set the **Sensitivity** value for the noisy potentiometer as high as needed to stop the continuous updates. A higher sensitivity value means a larger change in value is required before MobiFlight processes an update.

> [!TIP]
> Changes to the **Sensitivity** setting are not applied until uploaded to the board with the **Upload config** button.

### Improve the hardware

If reducing sensitivity is not sufficient, the following hardware improvements can reduce electrical noise on the potentiometer:

- Use shielded cables between the potentiometer and the board.
- Apply copper tape around the wiring to act as a shield.
- Install a small capacitor (typically 0.1 µF) between the potentiometer wiper pin and ground.

{{% /steps %}}

## Reducing noise from game controllers

For game controllers, use the device's configuration software or Windows joystick calibration to add a dead zone to the noisy axis.

{{% steps %}}

### Use the manufacturer software

If the device has dedicated configuration software, use it to set a dead zone and calibrate the endpoints of the noisy axis. For WinCtrl devices, use **SimAppPro** to calibrate the axis.

### Use Windows joystick calibration

If no manufacturer software is available, use the Windows game controllers control panel to set a deadzone for the noisy axis:

1. Search for and open **Setup USB game controllers** from the Windows start menu.
2. Double-click on the game controller causing the noisy inputs.
3. Use the **Deadzones** tab to add a small deadzone at the center point of the range for the noisy inputs.
4. Click **OK** to apply the settings.

{{% /steps %}}
