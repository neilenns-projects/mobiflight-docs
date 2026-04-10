---
title: WASM module disconnecting
description: Troubleshooting a constantly disconnecting WASM module caused by noisy inputs.
weight: 10
---

The WASM module can disconnect repeatedly when an input is sending a continuous stream of updates to MobiFlight, even when the input is not being touched. This is most commonly caused by:

- A noisy potentiometer connected to an Arduino board.
- An uncalibrated USB HID device, such as a game controller with analog inputs like the centering potentiometer in a WinCtrl EFIS or the photosensors in a WinCtrl autopilot panel.

## Identifying the noisy input

Enabling logging and watching the log output makes it easy to spot an input that is sending continuous updates.

{{% steps %}}

### Enable info logging

Follow the [logging guide](/guides/sharing-logs/) to enable **Info** logging.

### Open the log window

In the main MobiFlight window, click **View** then **Log** to open the log window.

### Watch for unexpected input events

Without touching any inputs, watch the log for entries showing input values changing on their own. A noisy input will produce a steady stream of log entries even when nothing is being moved.

### Identify the device

Note the module name and device listed in the log entries. This is the noisy input that needs to be addressed.

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

## Reducing noise from USB HID devices

For USB HID devices such as game controllers, use the device's configuration software or Windows joystick calibration to add a dead zone to the noisy axis.

{{% steps %}}

### Use the manufacturer software

If the device has dedicated configuration software, use it to set a dead zone and calibrate the endpoints of the noisy axis. For WinCtrl devices, use SimAppPro to calibrate the axis.

### Use Windows joystick calibration

If no manufacturer software is available, use the Windows joystick calibration tool to set a dead zone for the noisy axis:

1. Open **Control Panel** and navigate to **Devices and Printers**.
2. Right-click the game controller and select **Game controller settings**.
3. Select the controller and click **Properties**.
4. On the **Settings** tab, click **Calibrate** and follow the wizard to set the dead zone and endpoint values for the axis.

{{% /steps %}}

## Adding a software dead zone

If calibration alone does not stop the noise, use the [interpolation modifier](/features/modifiers/interpolation/) in the output configuration to map the noisy input range to a fixed output value, creating a software dead zone at the center or endpoints of the axis.
