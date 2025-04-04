---
title: Configuring outputs
description: Step-by-step guide for configuring game controllers as an output in MobiFlight.
aliases:
  - /joysticks/configuring-output/
weight: 20
---

MobiFlight supports using game controller LEDs as output devices for a select set of joysticks, including the Honeycomb Bravo Throttle Quadrant, Octavi, and VKBsim controllers.

Joystick outputs are configured in MobiFlight using [the LED device configuration process](/devices/led/configuring-input).

{{% steps %}}

### Select the board and device type for the output

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected game controller and the **LED / Output** device type.

{{< screenshot image="output-config-select-device.png" title="Screenshot of the display tab in the output dialog with a joystick and LED / Output type selected." >}}

### Select the LED to use for display

Use the **Select Pins** dropdown to select the LED that should display the output value.

{{< screenshot image="output-config-select-pins.png" title="Screenshot of the display tab in the output dialog with an LED output selected in the select pins dropdown." >}}

{{% /steps %}}
