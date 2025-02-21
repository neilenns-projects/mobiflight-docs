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

{{< schematic image="encoder-single.svg" download="encoder-single.pdf" title="Schematic for wiring a single encoder with an integrated button." >}}

{{< /tab >}}

{{< tab >}}

A dual encoder with an integrated button is similar to a single encoder, with an extra set of three pins on the button side for the outer encoder.

Each side is wired in the same fashion as a single encoder, with the outermost pins going to digital input pins on the board and the middle pin connecting to ground. In a schematic, pins for the inner encoder are referred to as `A`, `B`, and `C`. The pins for the outer encoder are referred to as `A'`, `B'` and `C'`.

The button pins are `S1` and `S2`, and connect to the board the same way as a single encoder button.

{{< schematic image="encoder-dual.svg" download="encoder-dual.pdf" title="Schematic for wiring a dual encoder with an integrated button." >}}

{{< /tab >}}

{{< /tabs >}}
