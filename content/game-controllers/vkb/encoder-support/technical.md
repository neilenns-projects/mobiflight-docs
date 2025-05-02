---
title: Encoder Technical Details
description: Technical details of VKB encoder integration
prev: /game-controllers/vkb/
weight: 10
---
Each encoder detected on the controller is added as a pair of virtual buttons. To avoid conflict with standard game controller buttons, which are in the range from 1 to 128, the virtual encoder buttons are mapped to the range of 1000-1319.

This number is based on the ID of the encoder, assigned automatically in ascending order from 0 to 31, and the direction the encoder is turned in.

For example, for increasing the third encoder on a device (e.g. turning En1 on a STECS Standard clockwise), the button ID would look like this:

| Digit | Meaning              | Details                  | Example |
| ----- | -------------------- | ------------------------ | ------- |
| 1     | Prefix               | Always 1                 | 1       |
| 2     | Encoder ID 1st digit | 10s place                | 0       |
| 3     | Encoder ID 2nd digit | 1s place                 | 2       |
| 4     | Direction            | 0: Decrease, 5: Increase | 5       |

The encoder would thus be treated as "Button 1025".

The mapping between physical movement of the knob and increase/decrease directions is determined by the hardware.
