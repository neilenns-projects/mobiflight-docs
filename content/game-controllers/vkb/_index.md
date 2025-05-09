---
title: VKB devices
description: How to use VKB devices with MobiFlight.
next: /game-controllers/vkb/led-support/
weight: 60
---
MobiFlight supports all VKB controllers and their axes, buttons and hat switches as generic game controller inputs. This includes limited encoder support as buttons.

MobiFlight also supports advanced functionality like LED control and improved support for rotary encoders. Depending on your controller, this may require preparation.

As with all game controllers, VKB controllers are not MobiFlight [boards](/boards/), and will therefore not appear in the **Modules** tab of the **Settings** dialog. Their [inputs](/game-controllers/configuring-input/) are automatically available in the MobiFlight configuration dialog.

LED [outputs](/game-controllers/configuring-output/) on VKB controllers are supported where controller definitions are available.

> [!NOTE]
> Support for LEDs requires that your VKB controllers are running firmware version 2.08.5 or newer.

Controllers with definitions available will also provide friendly names for inputs. Due to the modular nature of VKB controllers, it is not possible to include definition files for every possible controller configuration. If your controller configuration does not have an included definition file, [tools and guides](/game-controllers/vkb/create-definition/) are available to create your own.

> [!NOTE]
> The included definitions for STECS throttles are designed for the button module combinations that come out of the box on a STECS Mk1. Otherwise, buttons on the right grip, STEM and any add-on modules may be mislabeled.  
> For STECS Mk2 throttles, {{< a href="MTGR_Mk2.zip" download="MTGR_Mk2" >}}alternative definition files{{< /a >}} are available. Extract the file into the `Joysticks` folder of your MobiFlight installation, e.g. into `%LOCALAPPDATA%\MobiFlight\MobiFlight Connector\Joysticks`.  
> For custom button module combinations, a new definition file must be [created](/game-controllers/vkb/create-definition/).

The rotary encoder functionality can be greatly enhanced if the device is [properly configured](/game-controllers/vkb/encoder-support/) in VKBDevCfg to allow more responsive behavior.
