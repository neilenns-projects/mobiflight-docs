---
title: Finding encoder IDs
description: How to find the ID corresponding to a physical encoder using the Encoder Visualizer tool.
prev: /game-controllers/vkb/encoder-support/
next: /game-controllers/vkb/encoder-support/technical/
weight: 10
---
To determine the ID of an encoder on VKB controllers, the [Encoder Visualizer program](https://github.com/cbrauers/EncoderVisualizer/releases/latest) can be used:

{{% steps %}}

### Startup

Ensure that your VKB controller is connected and that advanced encoder support is [enabled](/game-controllers/vkb/encoder-support) on the controller.

Download, extract and run the latest release of Encoder Visualizer from the link above.

### Select controller

Select the tab corresponding to the controller you want to identify encoders on.

### Move the encoder knob

{{< screenshot image="encoder-visualizer.png" title="Encoder Visualizer main window." >}}

In the window you see knobs corresponding to each encoder ID. When you turn the physical knob, the knob with the corresponding ID will turn with it. It will turn clockwise on an increasing turn and counterclockwise on a decreasing turn. The ID is spelled out on top of the encoder's box.

The hexadecimal number shown underneath the knob is the raw data reported by the controller.

{{% /steps %}}
