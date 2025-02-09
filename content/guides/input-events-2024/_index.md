---
title: Finding input events in MSFS2024
description: Step-by-step guide to finding input events in Microsoft Flight Simulator 2024 for use with MobiFlight.
---

Input events are the way to interact with Microsoft Flight Simulator 2024 from apps like MobiFlight. Also referred to as `Bvars`, they provide a defined way to trigger every cockpit interaction.

Input events for Microsoft Flight Simulator 2024 are documented in [HubHop](https://hubhop.mobiflight.com/) under each aircraft with `(2024)` appended to the end. For example, Cessna 172 input events are under the [`C172 (2024)`](https://hubhop.mobiflight.com/presets/?aircraft=C172+%282024%29) aircraft.

The following steps illustrate how to find the input event for the parking brake in a Cessna 172 for use with a [toggle switch](/devices/button-switch/).

{{% steps %}}

### Enable developer mode

In Microsoft Flight Simulator 2024 settings, select the **Advanced Options** section then enable the **Developer Mode** option.

{{< screenshot image="advanced-options.png" title="Screenshot of Microsoft Flight Simulator 2024 settings with the Advanced Options section and Developer Mode option highlighted." >}}

### Spawn the plane

Use **Free Flight** mode to spawn the Cessna 172 at an airport.

### Open the behaviors window

From the **Tools** menu select **Behaviors**.

{{< screenshot image="behaviors-menu.png" title="Screenshot of the Tools menu open with the Behaviors menu item highlighted." >}}

When the behaviors window opens it will look like this:

{{< screenshot image="behaviors-window.png" title="Screenshot of the Behaviors window after opening it via the menu." >}}

### Find the input event

Aircraft often have hundreds of input events, sometimes with names that aren't clear, making it challenging to find the correct one. A simple way to quickly locate the correct event is to look it up with a keyboard shortcut.

To find the input event for the parking brake place the mouse cursor over the parking brake handle in the cockpit then press **CTRL + G** on the keyboard.

{{< screenshot image="parking-brake.png" title="Screenshot of the aircraft with the parking brake handle highlighted in red and CTRL + G next to it." >}}

After pressing the keyboard shortcut the behaviors window will update to show basic information about the parking brake.

{{< screenshot image="after-ctrl-g.png" title="Screenshot of the behaviors dialog with the Inspector tab open for the parking brake." >}}

### Open the input event details

To view the input events associated with the parking brake, click the **InputEvents** section to expand it.

{{< screenshot image="input-events-expanded.png" title="Screenshot of the behaviors dialog with the **InputEvents** section expanded and the input event highlighted with a red rectangle." >}}

Once the section is expanded click the **LANDING_GEAR_PARKINGBRAKE** button to open the **InputEvents** tab with all the events associated with the parking brake handle.

### Expand the input events tab

By default the **InputEvents** tab hides the important information in a collapsed section. To view all the input events associated with the parking brake click the **LANDING_GEAR_PARKINGBRAKE** header to expand the collapsed information.

{{< screenshot image="input-events-tab-expanded.png" title="Screenshot of the Behaviors dialog InputEvents tab with the LANDING_GEAR_PARKINGBRAKE section highlighted with a red rectangle and expanded." >}}

### Identify the correct input event

Controls in Microsoft Flight Simulator have multiple input events, even for simple controls like a parking brake.

The **Bindings** section lists the input events used with MobiFlight. In this example there are six different events shown:

- LANDING_GEAR_PARKINGBRAKE_Inc
- LANDING_GEAR_PARKINGBRAKE_Dec
- LANDING_GEAR_PARKINGBRAKE_Set
- PARKING_BRAKES
- PARKING_BRAKE_SET
- LANDING_GEAR_PARKINGBRAKE_TOGGLE

The suffix at the end of each event is a good indicator of its intended use. Events ending in `Inc` and `Dec` are useful when mapping controls to a [rotary encoder](/devices/encoder/). Events ending in `TOGGLE` are useful when mapping controls to a [push button](/devices/button-switch/). Events ending in `Set` are useful when mapping controls to a [toggle switch](/devices/button-switch/). While not available for the parking brake, `ON` and `OFF` events are common as well.

### Testing the LANDING_GEAR_PARKINGBRAKE_Set event

Since the parking brake will get mapped to a toggle switch, with a specific `on` and `off` position, the **LANDING_GEAR_PARKINGBRAKE_Set** event is likely the correct one to use with MobiFlight.

To test it, expand the event to see the parameters and **Execute** button.

{{< screenshot image="input-events-set-expanded.png" title="Screenshot of the Behaviors dialog InputEvents tab with the LANDING_GEAR_PARKINGBRAKE_Set binding expanded and highlighted with a red rectangle." >}}

The event takes a single parameter to set the parking brake state. In most cases, events that turn something on and off use `1` as the parameter to indicate on and `0` to indicate off.

This assumption can be tested by entering a **`1`** in the parameter box and pressing the **Execute** button. The parking brake in the simulator should move to the on position. Entering a **`0`** in the parameter box and pressing the **Execute** button should move the parking brake to the off position.

### Using the event in MobiFlight

With the event tested and working it can now be converted to the correct format for use in MobiFlight. Copy the event name by right clicking on it and selecting **Copy to Clipboard**.

{{< screenshot image="copy-to-clipboard.png" title="Screenshot of the Behaviors dialog InputEvents tab with the context menu open on the LANDING_GEAR_PARKINGBRAKE_Set binding and Copy to Clipboard highlighted." >}}

In MobiFlight create a new input configuration and select the appropriate switch as the device. Set the **Action Type** for **On Press** to **Microsoft Flight Simulator** and check the **Show Preset Code** box. The preset code box is where the event will go.

{{< screenshot image="input-config-show-preset-code.png" title="Screenshot of a MobiFlight input configuration with the Show Preset Code checkbox checked." >}}

The event needs to be converted to [RPN](https://docs.flightsimulator.com/html/Additional_Information/Reverse_Polish_Notation.htm) format for use as a custom preset. For the **On Press** event, where the input event gets set to `1`, use the following custom code:

```RPN
1 (>B:LANDING_GEAR_PARKINGBRAKE_Set)
```

{{< screenshot image="input-config-on-press.png" title="Screenshot of a MobiFlight input configuration with the custom code for setting the parking brake." >}}

For the **On Release** event use the following custom code:

```RPN
0 (>B:LANDING_GEAR_PARKINGBRAKE_Set)
```

Notice how the event name discovered in the previous steps is wrapped with `(>B:` and `)`, and `1` and `0` are used to set and release the parking brake. This pattern applies for any input event that takes a value.

### Close the dialog and try it out

Click the **OK** button to close the dialog.

Make sure the MobiFlight **Run** button is clicked in the toolbar, then try toggling the parking brake with the switch. The parking brake in the simulator should toggle.

{{% /steps %}}
