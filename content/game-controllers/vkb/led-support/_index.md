---
title: LED support
description: Information about LED support.
prev: /game-controllers/vkb/
next: /game-controllers/vkb/led-support/led-ids/
weight: 10
---

LED support for VKB controllers in MobiFlight requires no preparation in VKBDevCfg if your firmware is version 2.08.5 or higher. Just configure your device as you usually would.

A definition file ensures the MobiFlight Connector application knows the LEDs on the device, their IDs, and colors. Many definition files are included; for customized setups, you may need to [create your own definition file](/game-controllers/vkb/create-definition).

LEDs on VKB devices can broadly be classified into three different categories based on their available colors:

### Monochrome LEDs

A few LEDs on VKB controllers only support a single color. These are integrated in MobiFlight as straightforward LED outputs.

### Bi-color LEDs

The bi-color LED is the most common type of LED used in MobiFlight configurations for VKB devices. The power/status LED on most VKB controllers is bi-color blue/red, and the numerous indicator LEDs on the GNX module series all use green/red bi-color LEDs.

Bi-color LEDs have each physical color assigned to one of the internal color channels, being able to display either color, as well as a mix of the two. Each color channel is integrated as a distinct LED output in MobiFlight. The intensity sent to the controller is controlled such that if both the red and green channels of a GNX LED are on, the resulting mix will result in an amber color.

When both the red and green channels of the LEDs are off, zero brightness is sent instead of an off event to override the default green of unused LEDs on GNX modules.

### RGB LEDs

RGB LEDs allow control of three primary colors. Each of the three color channels is integrated in MobiFlight as an LED output.
