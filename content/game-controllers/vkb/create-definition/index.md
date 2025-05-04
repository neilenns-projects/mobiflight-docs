---
title: Create definition file
description: Creating a definition file for new devices.
prev: /game-controllers/vkb/encoder-support/encoder-ids/
weight: 20
---
Not every combination of VKB modules has a pre-made definition file available. To enable support for LED outputs and friendly names in such a configuration, it is necessary to create a new definition file.

To help with the creation of such files, the [VKB/MobiFlight Definer tool](https://github.com/cbrauers/VKB-Mobiflight-Definer/releases/latest) can build a file for the default configuration of most controller combinations:

{{% steps %}}

### Startup

Ensure that your VKB controller is connected and MobiFlight is not running.

Download, extract and run the latest release of the definer tool from the link above.

### Select controller

{{< screenshot image="definer-devices.png" title="Device list in definer tool." >}}

Select your VKB controller from the list of controllers shown by entering the number of the list entry and pressing the enter key.

### Select the base

{{< screenshot image="definer-bases.png" title="List of bases as shown in definer tool." >}}

Select your base from the list by typing the corresponding number and pressing enter.

Some bases may contain extension modules like grips or the ATEM. That is because these modules affect the button mapping on the base or act as an extension to the base.

If your controller is a GNX throttle combo, the base unit is the GNX-HID USB Controller.

### Select add-on modules

{{< screenshot image="definer-addons.png" title="List of modules as shown in definer tool." >}}

Select each module that is part of your controller. If you have multiples of the same module, add the same module type multiple times.

It is generally recommended to follow the order in this list:

- Grips
- SEM
- THQ
- STEM
- FSM.GA

For STECS split throttle grips, choose the left grip first. If one of your THQs has a WW2 throttle grip, choose that one last. There is no distinction between SEM and SEM-V, or between THQ and THQ-V.

Once all modules have been added, select option zero and proceed with [step 9, **Enable encoder API**](#enable-encoder-api)

### Select grip preset

This step is for the STECS MTG-R. For other modules, skip to [step 7, **Enter first button ID**](#enter-first-button-id).

{{< screenshot image="definer-stecs-preset.png" title="List of STECS MTG-R presets." >}}

Since the STECS MTG-R allows for swappable button modules, this menu allows you to choose the button modules installed in your grip. Common grip configurations are prepared as presets, but you can also choose a fully custom preset by typing in 0.

> [!TIP]
> You can base a custom configuration off an existing preset by entering the number with a leading zero, e.g. `05`.

### Select button modules

{{< screenshot image="definer-stecs-button-modules.png" title="List of STECS button modules." >}}

If you selected a custom preset, you will be prompted which modules are installed in each slot. Enter the number in the list and continue. The list will change between modules to reflect the valid modules for each slot.

Repeat this step until all module slots are filled.

### Enter first button ID

{{< screenshot image="definer-module-buttons.png" title="Button ID prompt." >}}

Enter the ID of the first button of the current module. A label to find that button is shown in the prompt.

If you are following the controller order mentioned in [step 4, **Select add-on modules**](#select-add-on-modules), the default is usually correct, but you can always verify in a button tester application.

### Enter first LED ID

{{< screenshot image="definer-module-leds.png" title="LED ID prompt." >}}

Enter the base LED ID of the first module. It can be looked up in the VKBDevCfg external controller tab.

If you are following the controller order mentioned in [step 4, **Select add-on modules**](#select-add-on-modules), the default is usually correct.

Return to [step 4, **Select add-on modules**](#select-add-on-modules) to continue setting up further modules.

### Enable encoder API

{{< screenshot image="definer-encoder-api.png" title="Enable the encoder API." >}}

If any of your controller components feature rotary encoders, you will be asked to enable the rotary encoder API. This is required for the advanced encoder feature and generally does not come with drawbacks. It is recommended to accept this.

### Enter encoder IDs

{{< screenshot image="definer-encoder-id.png" title="Encoder ID prompt." >}}

Enter the ID of the encoder described in the prompt.

If you are following the controller order mentioned in [step 4, **Select add-on modules**](#select-add-on-modules), the default is usually correct.

When in doubt (perhaps because you have added shift states to encoders in VKBDevCfg), an encoder visualizer application is available to test which encoder ID represents which encoder. Complete this step until all encoders are assigned an ID.

### Copy file

{{< screenshot image="definer-done.png" title="Finished creating definition file." >}}

The utility will inform you that the file has been created. You can find it in the output folder of the definer application.

> [!NOTE]
> While this definition file will be suitable for automatically configured VKB devices, some configuration edits, like changing logical button IDs, may require manual edits to the definition file.

Copy the file to the `Joysticks` folder in your MobiFlight installation directory.

> [!TIP]
> If you used the MobiFlight Setup from the MobiFlight website, you can find the destination folder by entering `%LOCALAPPDATA%\MobiFlight\MobiFlight Connector\Joysticks` into the address bar.

{{% /steps %}}
