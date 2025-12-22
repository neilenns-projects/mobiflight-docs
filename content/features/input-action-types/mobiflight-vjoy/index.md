---
title: MobiFlight - Virtual Joystick input (vJoy)
description: How to use the MobiFlight - Virtual Joystick input (vJoy) action type with MobiFlight.
aliases:
  - /guides/input-action-types/mobiflight-vjoy/
weight: 50
---

The **MobiFlight - Virtual Joystick input (vJoy)** action type triggers a vJoy input, simulating a joystick input. This action type is typically used to interact with applications other than a flight simulator, for example to trigger push-to-talk in [vPilot](https://vpilot.rosscarlson.dev/) or [xPilot](https://docs.xpilot-project.org/).

> [!IMPORTANT]
> This action type requires vJoy. Many versions are available online, not all of which work with modern versions of Windows. The [BrunnerInnovation fork](https://github.com/BrunnerInnovation/vJoy/releases/tag/v2.2.2.0) is known to work on both Windows 10 and Windows 11.

{{< screenshot image="mobiflight-vjoy.png" title="Screenshot of a button input with the MobiFlight - Virtual Joystick input (vJoy) action type selected." >}}

| Setting     | Description                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------ |
| Joystick ID | The virtual joystick to trigger.                                                                             |
| Button Nr   | The virtual button to trigger.                                                                               |
| Axis        | The virtual axis to set.                                                                                     |
| Button      | The state to set the button to, either **on** or **off**.                                                    |
| Value       | The value to set the axis to. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/) |
