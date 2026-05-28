---
title: Using the selector knob on a Honeycomb Bravo
description: Step-by-step guide to using the Honeycomb Bravo selector knob with a MobiFlight profile.
---

The Honeycomb Bravo's autopilot inputs rely on a selector knob to indicate what autopilot feature the right knob controls. MobiFlight pre-conditions can be used to configure the appropriate events for the right knob based on the selector knob position.

A sample file that implements this is available. It provides all the input configs necessary to make this work, however you'll have to edit all the knob inputs to specify what events you actually want to have happen when the knob is turned.

This same technique can be used to do things like display different radios on a 7-segment display based on a knob position, or to use a single encoder with a toggle button to change different radio frequencies.

Want to build the file yourself and understand how it works? Here's how to do it.

{{% steps %}}

### Create input configurations for the ALT selector knob position

1. Create a new input config called `Selector - ALT`
2. Set the module to `Bravo Throttle Quadrant` and the device to `Mode - ALT`
3. For the `On Press` event select `MobiFlight - Variable` for the `Action Type`
4. Set the variable name to `Selector`
5. Set the value to `0`

The input config should look like this:

{{< screenshot image="alt-position-input-config.png" title="Screenshot of the input config wizard configured for the ALT selector knob." >}}

### Create input configurations for the other selector knob positions

Repeat step 1 four more times, updating the name to and device to reflect the switch position (`VS`, `HDG`, etc.) and incrementing the value by one for each switch position. When you are done you should have five input configurations that set the `Selector` variable to the following values:

| Input name     | Device     | Variable value |
| -------------- | ---------- | -------------- |
| Selector - ALT | Mode - ALT | 0              |
| Selector - VS  | Mode - VS  | 1              |
| Selector - HDG | Mode - HDG | 2              |
| Selector - CRS | Mode - CRS | 3              |
| Selector - IAS | Mode - IAS | 4              |

Your input config tab should look like this:

{{< screenshot image="main-window-selector-knob-configs.png" title="Screenshot of the main MobiFlight window with the selector knob configs added." >}}

### Create an input config for a left turn of the right knob when ALT mode is active

Start by adding the precondition:

1. Create a new input config called `Right knob - ALT decrement`
2. On the `Precondition` tab click on `<none>` in the precondition list
3. Set the `Use type of` dropdown to `MobiFlight Variable`
4. Set the `Choose variable` dropdown to `Selector
5. Set the value to 0

The precondition tab should look like this:

{{< screenshot image="alt-precondition.png" title="Screenshot of the precondition tab for the right knob - ALT decrement input config." >}}

Then add the input device:

1. Switch to the `Input` tab for the config
2. Select `Bravo Throttle Quadrant` from the `Module` dropdown
3. Select `Encoder - Left` from the `Device` dropdown
4. Configure the `On Press` event to do whatever event you want
5. Save the config

The input tab should look like this:

{{< screenshot image="alt-device-assignment.png" title="Screenshot of the device tab for the right knob - ALT decrement input config." >}}

> [!TIP]
> The above example illustrates mapping the ALT decrement action to the Cessna CJ4 autopilot ALT decrement event in Microsoft Flight Simulator 2024. When building your own profile, adjust the selected event to match the appropriate one for your aircraft.

### Create an input config for a right turn of the right knob when ALT mode is active

Repeat everything in step 3, except select `Encoder - Right` from the `Device` dropdown and name the input `Right knob - ALT increment`.

### Create the increment and decrement configs for the other four knob positions

Repeat everything in step 3 and 4 except when configuring the precondition use the appropriate number from the table in step 2. For example, if you are creating the increment and decrement configs for `CRS` you would use `3` for the precondition value. Make sure to name the configs appropriately as well (e.g. `Right knob - CRS decrement`).

When you are done your input config tab should look like this:

{{< screenshot image="all-configs.png" title="Screenshot of the main MobiFlight window with all the input configs created." >}}

### Create an output config for the selector (optional)

To assist with debugging it can be helpful to have an output config that references the `Selector` variable. To do this create an output config that looks like this:

{{< screenshot image="output-config.png" title="Screenshot of an output config set up to display the value of the selector knob variable." >}}

There's no need to actually display it on any output device. This basic output config will show the value in the main Mobiflight window:

{{< screenshot image="main-window-output-config.png" title="Screenshot showing the main MobiFlight window with the selector output configuration highlighted and showing a current value of 1." >}}

MobiFlight also indicates which of the input configs are inactive by showing a purple `!` icon next to configs that are disabled by the precondition value. In the above screenshot, the `VS` inputs are active and the rest are disabled.

{{% /steps %}}
