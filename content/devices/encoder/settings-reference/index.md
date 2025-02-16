---
title: Settings reference
description: Description of all available settings for rotary encoder devices and input configurations using encoders.
ogimage: card-images/devices/encoder-single.png
weight: 50
---

## Modules dialog

{{< screenshot image="encoder-configuration.png" title="Screenshot of the Modules dialog with the encoder configuration showing." >}}

| Setting   | Description                                                                                                                                                                                                                                                                                                                                                                                                            |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Left pin  | The board pin connected to the left output pin on the encoder. All digital and analog pins are supported.                                                                                                                                                                                                                                                                                                              |
| Right pin | The board pin connected to the right output pin on the encoder. All digital and analog pins are supported.                                                                                                                                                                                                                                                                                                             |
| Swap      | When pressed, swaps the left and right pin assignments.                                                                                                                                                                                                                                                                                                                                                                |
| Type      | The number of detents and data signal order of the encoder. **1 detent per cycle (11)** and **2 detents per cycle (00, 11)** are the most common encoder types. [Encoders from the MobiFlight shop](https://shop.mobiflight.com/product/rotary-encoder-ec11) are **2 detents per cycle (00, 11)**. If the encoder skips steps with the selected type, try each of the other types until the correct one is identified. |
| Name      | The name for the encoder. Displayed in the input configuration dialog to identify the encoder when mapping the left and right inputs to simulator events.                                                                                                                                                                                                                                                              |

> [!TIP]
> Changes to the **Type** setting are not applied until uploaded to the board with the **Upload config** button.

## Input configuration

{{< tabs items="On Left, On Left (Fast), On Right, On Right (Fast)" >}}

{{< tab >}}

The **On Left** event fires when the encoder is turned to the left.

{{< screenshot image="on-left.png" title="Screenshot of the encoder On Left event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Left (Fast)** event fires when the encoder is turned to the left quickly.

{{< screenshot image="on-left-fast.png" title="Screenshot of the encoder On Left (Fast) event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Right** event fires when the encoder is turned to the right.

{{< screenshot image="on-right.png" title="Screenshot of the encoder On Right event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< tab >}}

The **On Right (Fast)** event fires when the encoder is turned to the right quickly.

{{< screenshot image="on-right-fast.png" title="Screenshot of the encoder On Right (Fast) event tab with the Action Type menu opened." >}}

{{< /tab >}}

{{< /tabs >}}
