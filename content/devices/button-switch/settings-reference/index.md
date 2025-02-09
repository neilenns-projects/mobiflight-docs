---
title: Settings reference
description: Description of all available settings for button devices and input configurations using buttons.
ogimage: card-images/devices/switch.png
weight: 40
---

## Modules dialog

{{< screenshot image="button-configuration.png" title="Screenshot of the Modules dialog with the button configuration showing." >}}

| Setting | Description                                                                                                                                     |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| Pin     | The board pin connected to the button. All digital and analog pins are supported.                                                               |
| Name    | The name for the button. Displayed in the input configuration dialog to identify the button when mapping the button input to a simulator event. |

## Input configuration

{{< tabs items="On Press, On Release, On Hold, On Long Release" >}}

{{< tab >}}

The **On Press** event fires immediately after the button is pressed.

> [!NOTE]
> This event is always sent, even if the button is held long enough to trigger the **On Hold** event.

{{< screenshot image="on-press.png" title="Screenshot of the button On Press event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Release** event fires when the button is released, as long as **On Long Release** is not configured. If **On Long Release** is configured, **On Release** will fire when the button is held for less than the on long release duration.

{{< screenshot image="on-RELEASE.png" title="Screenshot of the button On Release event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Hold** event always fires when the button is held for longer than the millisecond count specified in the **Delay** field.

If the **repeat every** value is non-zero, the event will fire repeatedly at the specified millisecond interval.

{{< screenshot image="on-hold.png" title="Screenshot of the button On Hold event tab with the delay set to 350 ms, repeat every set to 0 ms, and the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Long Release** event fires when the button is released after being held for longer than the millisecond count specified in the **Delay** field.

{{< screenshot image="on-long-release.png" title="Screenshot of the button On Long Release event tab with a 350 ms delay specified and the Action Type menu opened." >}}

{{< /tab >}}
{{< /tabs >}}
