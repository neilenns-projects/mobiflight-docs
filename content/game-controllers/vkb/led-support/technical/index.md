---
title: LED technical details
description: Technical details of VKB LED integration.
prev: /game-controllers/vkb/led-support/led-ids/
next: /game-controllers/vkb/encoder-support/
weight: 20
---
 VKB device integration leverages the definition format from MobiFlight’s generic LED system, which is designed to control LEDs via bit fields similar to those on the Honeycomb Bravo Throttle Quadrant. Terminology is repurposed to keep the file format compatible.

In definition files, an LED is identified by `Label`, `Id`, `Byte` and `Bit` properties. **Label** and **Id** are self-explanatory as human-readable and machine-readable names for the LED, respectively.

The **Byte** field contains the LED ID used on the controller. It typically ranges between 0 and 9 for base LEDs and between 10 and 63 for module LEDs.

The **Bit** field identifies the color channel. Monochrome LEDs have only channel 0; bi-color LEDs use channels 0 and 1 for their two colors; and RGB LEDs use channels 0, 1, and 2 to drive red, green, and blue, respectively.

Special handling for green/red LEDs is done by checking the **Id** field of channel 0. If it ends in **G**, it is a green/red LED. This is required to facilitate the mixing of an amber color if both green and red light up at the same time.

The LED integration does not support VKB's built-in blinking or alternate color functionalities. It is also limited to on/off LEDs with no support for VKB's 3-bit dimming.
