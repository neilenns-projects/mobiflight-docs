---
title: Wiring
description: Step-by-step guide to wiring encoders.
ogimage: card-images/devices/encoder-both.png
weight: 10
prev: /devices/encoder/
---

{{< tabs items="Single encoder with button,Dual encoder with button" >}}

{{< tab >}}

A single encoder with an integrated button has three legs on one side that connect the encoder and two legs on the other side that connect the button. The outer legs of the encoder side are connected to digital inputs on the board. The middle pin is connected to ground.

One leg on the button side is connected to a digital input on the board. The other leg is connected to ground. It doesn't matter which button leg goes to ground and which goes to the board.

{{< schematic image="encoder-single.svg" title="Schematic for wiring a single encoder with an integrated button." >}}

{{< /tab >}}

{{< tab >}}

A dual encoder with an integrated button is similar to a single encoder, however there are two rows of three legs on the encoder side. One row controls the outer encoder, the other row controls the inner encoder.

Each row is wired in the same fashion as a single encoder, with the outer legs going to digital input pins on the board and the middle pin connecting to ground. In a schematic, the row of pins for one of the encoders is referred to as `A`, `B`, and `C`. The row of pins for the second encoder is referred to as `A'`, `B'` and `C'`.

The button side of the dual encoder connects to the board the same way as a single encoder button.

{{< schematic image="encoder-dual.svg" title="Schematic for wiring a dual encoder with an integrated button." >}}

{{< /tab >}}

{{< /tabs >}}
