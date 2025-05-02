---
title: VKB devices
description: How to use VKB devices with MobiFlight.
next: /game-controllers/vkb/encoder-support
weight: 60
---
MobiFlight supports all VKB controllers and their axes, buttons and hat switches as generic game controller inputs. Limited encoder functionality is also available as a generic game controller.

As with all game controllers, VKB controllers are not MobiFlight [boards](/boards/), and will therefore not appear in the **Modules** tab of the **Settings** dialog. Their [inputs](/game-controllers/configuring-input/) are automatically available in the MobiFlight configuration dialog.

LED [outputs](/game-controllers/configuring-output/) are supported for VKB controllers with available controller definitions.

> [!TIP]
> Support for LEDs requires that your VKB controllers are running firmware version 2.08.5 or newer.

Controllers with definitions available will also provide friendly names for inputs. Due to the modular nature of VKB controllers, it is not possible to include definition files for every possible controller configuration. If your controller configuration does not have an included definition file, tools and guides are available to create your own.

> [!TIP]
> The included definitions for STECS throttles are designed for the button module combinations that come out of the box on a STECS Mk1. Otherwise, buttons on the right grip, STEM and any add-on modules may be mislabeled.  
> For STECS Mk2 throttles, {{< a href="MTGR_Mk2.zip" download="MTGR_Mk2" >}}alternative definition files{{< /a >}} are available. Extract the file into the `Joysticks` folder of your MobiFlight installation, e.g. into `%LOCALAPPDATA%\MobiFlight\MobiFlight Connector\Joysticks`.  
> For custom button module combinations, a new definition file must be created.

The rotary encoder functionality can be greatly enhanced if the device is properly configured in VKBDevCfg to allow more responsive behavior.
