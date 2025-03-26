---
title: Troubleshooting
description: Troubleshooting potentiometer issues.
ogimage: card-images/devices/potentiometer.png
weight: 40
---

Potentiometers are generally reliable components, but slight variations between the different devices may cause problems when using standard events. This guide will help you troubleshoot common issues with potentiometers.

## Handling potentiometer noise

Potentiometers are sensitive devices that can pick up  electrical noise from the environment. This noise can cause the potentiometer to send random values to the simulator, even when the potentiometer is stationary.

If the simulator input is changing value even when the potentiometer is stationary, try reducing the **Sensitivity** setting in the [**Modules** dialog](/devices/potentiometer/settings-reference/#modules-dialog).

7-segment displays are a frequent source of interference that is challenging to eliminate. It can be reduced by installing capacitors on the display power input and the potentiometer. To completely eliminate noise from displays, move them to a separate board, away from the potentiometer.

## Adjusting the potentiometer range

While most 10kΩ linear potentiometers have a range of 0--1023, some may have a slightly different range. To verify the range of your potentiometer, [connect it to your board](/devices/potentiometer/wiring/), then take these steps.

{{% steps %}}

### Enable logging

Follow the [logging guide](/guides/sharing-logs/) to enable info logging.

### Move the potentiometer

Move the potentiometer from one end to the other.

### Write down the values

The log will show the values from the potentiometer. Write down the minimum and maximum values from the log.

In the example below, the lowest value produced by the potentiometer is 13. The highest value, not shown, is 1023.

{{< screenshot image="analog-input-log.png" title="Screenshot of the main MobiFlight window with the log window open and a potentiometer with a minimum value of 13 showing." >}}

{{% /steps %}}

> [!TIP]
> Don't forget to disable logging after obtaining the potentiometer values. Logging can slow MobiFlight down during normal use.

## Adjust the event range

If the range of your potentiometer is different from the standard 0--1023, use the [HubHop potentiometer tool](https://hubhop.mobiflight.com/tools/) to generate the correct custom input event.

{{% steps %}}

### Generate the event code

Set the **Device output range** preset to **Arduino** and enter the minimum and maximum values from the log. Set the **MSFS2020 event input range** to the desired input.

{{< screenshot image="hubhop-settings.png" title="Screenshot of the HubHop potentiometer tool with the values set for a 23 to 1023 potentiometer and a throttle input." >}}

### Use the event code

The generated event code will be shown in the **Generated RPN code** box.

{{< screenshot image="hubhop-generated-code.png" title="Screenshot of the HubHop potentiometer tool with the generated RPN code highlighted." >}}

Copy and paste the code as the preset code when **Show Preset Code** is checked in the [input configuration dialog](/devices/potentiometer/configuring-device/).

{{< screenshot image="custom-preset-code.png" title="Screenshot of the input configuration dialog with the Show Preset Code checkbox checked and the custom event code inserted." >}}

{{% /steps %}}
