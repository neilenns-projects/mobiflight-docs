---
title: Finding LED IDs
description: How to find the ID of an LED with VKBDevCfg.
prev: /game-controllers/vkb/led-support/
next: /game-controllers/vkb/led-support/technical/
weight: 10
---

### Identifying LEDs of a module

{{< screenshot image="vkb-leds-basenumber.png" title="Location of the LED settings for modules." >}}

In VKBDevCfg, navigate to **Global** on the bottom tab bar, then **External** on the top tab bar. Select the **External devices** tab on the left. For each connected module, there will be two spin boxes labeled **LedsN** and **Base** next to each other. The LedsN box contains the number of LEDs present on the module. The Base box contains the ID of the first LED of that module. The other LEDs follow in sequence.

### Identifying a specific LED

{{< screenshot image="zconfig-test-misc.png" title="Where to enable miscellaneous test functionality." >}}

To identify individual LEDs, you must first enable miscellaneous test functionality in VKBDevCfg. While the program is closed, open the `zconfig.ini` file in the VKBDevCfg directory in a text editor, find the line `[Common]`, add the line `Test Misc Enabled=1` underneath and save. Then open VKBDevCfg.

{{< screenshot image="vkb-leds-test-misc.png" title="Test Misc menu, including LED tests." >}}

In VKBDevCfg, when you select the **Test** tab at the bottom, you will see a **Misc** tab on top. Enter it and the LED test appears in the left half of the pane. In the top row, check the **Select** box and enter the ID of the LED you want to identify in the **LED #** box.

> [!TIP]
> To find out which ID belongs to a physical LED, try out the LED numbers belonging to its module. Be sure to set LEDs you already tried back to a neutral setting such as **OFF**.

For **LED MODE**, choose something recognizable like **Ultra fast**, which will cause the LED to blink rapidly. **COLOR MODE** can be **Color1** with **COLOR 1** set to **7:7:7**, i.e. white at maximum brightness. This will cause RGB LEDs to flash white, bi-color LEDs to flash in their primary color (e.g. green for green/red LEDs) and monochrome LEDs to flash in their only color.

Press the **Set Leds** button to make the light flash. To turn it off afterward, change **LED MODE** to **OFF** and press **Set Leds** again.
