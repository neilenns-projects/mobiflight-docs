---
title: Troubleshooting
description: Troubleshooting LCDs in MobiFlight.
ogimage: card-images/devices/lcd-20x4.png
weight: 50
---

LCDs are generally straightforward to use with MobiFlight. After connecting the display to a board and configuring it in MobiFlight, the text **MobiFlight Rocks!** should show. If the text does not display, check the following.

## Verify the pin assignments

LCDs can only be connected to specific pins on a board, typically labeled **SDA** and **SCL**. Check the pinout diagram on the [boards](/boards/) page and verify the LCD is connected to the appropriate pins.

## Adjust the contrast

All LCD driver boards have a potentiometer mounted to the back to adjust the contrast. LCDs often come with the contrast set so low it appears that the display isn't on at all.

To adjust the contrast, connect the LCD to a board and configure it in MobiFlight. Then, use a small screwdriver to turn the potentiometer until text is visible.

{{< screenshot image="contrast-potentiometer.png" title="Photo of the back of a 20x4 LCD with the potentiometer contrast adjustment highlighted in red." >}}
