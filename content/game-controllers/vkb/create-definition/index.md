---
title: Create definition file
description: Creating a definition file for new devices.
prev: /game-controllers/vkb/encoder-support
weight: 20
---
Not every combination of VKB modules has a pre-made definition file available. To enable support for LED outputs and friendly names in such a configuration, it is necessary to create a new definition file.

To help with the creation of such files, the [VKB/Mobiflight Definer tool](https://github.com/cbrauers/VKB-Mobiflight-Definer/releases/latest) can build a file for the default configuration of most controller combinations. Download, extract and run the latest release, then follow the on-screen prompts.

To create the definition file for a device, first select the USB device in question. Continue by choosing the base (which may include some grips and modules to streamline the process, depending on the hardware). When selecting different add-on controllers, it is generally recommended to follow the following order to get good defaults for button and LED numbers:

- Base, including everything listed in the description.
- Grips, starting from left to right for throttle grips.
- SEMs, including SEM-Vs.
- THQs, including THQ-Vs. If one of the THQs has a WW2 throttle grip, choose that one last.
- STEM
- FSM.GA

It is best to verify button numbers in a button tester application.

Once the program has completed, a file ending in `.joystick.json` will be available in the `output` folder. Copy this file to the `Joysticks` folder in your MobiFlight installation directory, e.g. `%LOCALAPPDATA%\MobiFlight\MobiFlight Connector\Joysticks`.

If you are running a heavily customized VKBDevCfg configuration, it may be necessary to make manual adjustments to the file to ensure button labels are accurate.
