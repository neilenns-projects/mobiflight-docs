---
title: Wiring
description: Step-by-step guide to wiring buttons and switches.
ogimage: card-images/devices/switch.png
weight: 10
prev: /devices/button-switch/
---

{{< tabs items="Tactile button,Two-position switch,Three-position switch" >}}

{{< tab >}}
Tactile buttons have one upper leg connected to a board pin and one lower leg connected to GND. The other two legs are left unconnected. No resistors are required.

{{< schematic image="tactile-button.svg" download="tactile-button.pdf" title="Wiring diagram showing a tactile button connected to a board." >}}
{{< /tab >}}

{{< tab >}}
Two-position switches have one outer leg connected to a board pin and the middle leg connected to GND. The second outer leg is left unconnected. No resistors are required.

If the switch has six pins instead of three (a DPDT switch), wire using one column of three pins and leave the other column disconnected.

{{< schematic image="two-position-switch.svg" download="two-position-switch.pdf" title="Wiring diagram showing a two-position switch connected to a board." >}}
{{< /tab >}}

{{< tab >}}
Three-position switches have both outer legs connected to separate board pins and the middle leg connected to GND. No resistors are required.

{{< schematic image="three-position-switch.svg" download="three-position-switch.pdf" title="Wiring diagram showing a three-position switch connected to a board." >}}

{{< /tab >}}

{{< /tabs >}}
