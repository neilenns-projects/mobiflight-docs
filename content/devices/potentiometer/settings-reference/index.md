---
title: Settings reference
description: Description of all available settings for potentiometer devices and input configurations using potentiometers.
ogimage: card-images/devices/potentiometer.png
weight: 40
---

## Modules dialog

{{< screenshot image="analog-input-configuration.png" title="Screenshot of the Modules dialog with the analog input configuration showing." >}}

| Setting     | Description                                                                                                                                                                                                                 |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pin         | The board pin connected to the button. Only analog pins are supported.                                                                                                                                                      |
| Sensitivity | The amount of change in value required before MobiFlight will process a value change. For example, a sensitivity of **10** means a value change of 10 is required before MobiFlight will process a new potentiometer value. |
| Name        | The name for the potentiometer. Displayed in the input configuration dialog to identify the potentiometer when mapping the input value to a simulator event.                                                                |

> [!TIP]
> Changes to the **Sensitivity** setting are not applied until uploaded to the board with the **Upload config** button.

## Input configuration

{{< tabs items="On Change" >}}

{{< tab >}}

The **On Change** event fires when the new value from the potentiometer exceeds previous value by the sensitivity set in the [**Modules** dialog](#modules-dialog).

The **@** symbol is replaced in the preset code with the value from the potentiometer. It can be used multiple times in the preset code, if necessary.

{{< screenshot image="on-change.png" title="Screenshot of the analog input On Change event tab with the THROTTLE1_SET preset for Microsoft Flight Simulator selected." >}}

{{< /tab >}}

{{< /tabs >}}
