---
title: Relays
description: How to use relays with MobiFlight.
ogimage: card-images/devices/relay.png
next: /devices/relay/wiring/
---

> [!CAUTION]
> Do not work with voltages over 24V unless you are familiar with electrical safety standards. AC mains voltage can cause serious injury or death if handled improperly. If you are unsure of how to work with AC mains voltage safely, consult a qualified electrician.

Relays are commonly used to switch electrical circuits running at more than +5V. They take an `on` or `off` signal as input to switch higher voltage on and off. For controlling LED strips with MobiFlight, use a [MOSFET](/devices/mosfet/) instead, as they provide the ability to dim the LEDs.

{{< cards >}}
{{< card title="Relays" image="card-images/devices/relay.png" >}}
{{</ cards >}}

To use relays with MobiFlight, follow the [LED guide](/devices/leds/) to configure them as outputs.

> [!TIP]
> Make sure to purchase 5V relays. Many listings include different variations, such as 12V, that will not work with [supported boards](/boards/).
