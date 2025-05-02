---
title: Encoder support
description: How to enable advanced encoder support.
prev: /game-controllers/vkb/
next: /game-controllers/vkb/create-definition/
weight: 10
---
While encoders are always available as joystick buttons out of the box, this indirect form of support suffers from limitations: Since each turn of the knob has to be turned into a button push and release, delays are incurred as the button pressing action catches up to the encoder position.

To circumvent this limit, MobiFlight can directly read the encoder position from the controller. For this to work, the controller must be configured in VKBDevCfg to make these positions available:

Close any running instance of MobiFlight and ensure your controller firmware is updated to version 2.18.5 or newer.

In VKBDevCfg, select your device, then open the **Global** tab at the bottom and the **External** tab at the top:

{{< screenshot image="vkb_tab.png" title="Location of the Global and External tabs." >}}

Make sure the checkboxes **Virtual BUS over USB** and **External device encoders virtualization** are both checked. Then write the configuration to the device by pressing the **Set** button in the **Action** bar.

{{< screenshot image="vkb_usb.png" title="Boxes to check." >}}

After you press **Set**, your device will disconnect and immediately reconnect to the PC. The next time you start MobiFlight, responsive encoder events will be available.

If your controller does not have a definition file (i.e. all buttons are listed as button numbers), the new encoder events will appear towards the end of the button list.

If your controller has a definition file with outputs and friendly input names, the new encoder events will replace the buttons used for the encoder. Note that the original button events are still available with a **Legacy DirectInput** mark for compatibility reasons, and that the **Scan for Input** function may latch onto those button events.
