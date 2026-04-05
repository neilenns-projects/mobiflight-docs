---
title: X-Plane DataRefs and commands
description: Overview of X-Plane DataRefs and commands and how to use them with MobiFlight.
---

MobiFlight interfaces with X-Plane using native X-Plane DataRefs and commands. Understanding what DataRefs and commands are, and how to find them, is key to configuring MobiFlight for X-Plane.

## DataRefs and commands

X-Plane provides two ways to interact with the simulator:

### DataRefs

DataRefs are simulator variables that provide access to state information from the aircraft, cockpit, and simulator, such as speed, altitude, altimeter reading, and warning lights. Use DataRefs in output configurations to read values from X-Plane. Some DataRefs are also writable, which allows them to be used in input configurations to set a specific value.

### Commands

Commands are for input actions only. They are simpler to use than writable DataRefs because they do not require a value to be specified. For example, a heading bug increment or decrement command does not require you to calculate the new heading value.

Both DataRefs and commands are identified by a path-structured name, for example:

- DataRef "Autopilot heading" - `sim/cockpit2/autopilot/heading_dial_deg_mag_pilot`
- Command "Boeing 737 autopilot heading decrement" - `laminar/B738/autopilot/heading_dn`

> [!TIP]
> Use commands for input actions when possible. Commands are simpler to configure because they do not require calculating a new value.

## Finding DataRefs and commands

### HubHop presets

The easiest way to find X-Plane DataRefs and commands is through the HubHop presets built into MobiFlight. When configuring an input or output, use the **Search**, **Vendor**, **Aircraft**, and **System** filters to find the preset you need.

> [!TIP]
> To update the HubHop preset list, select **Download Latest Presets** from the **Extras** > **HubHop** menu.

X-Plane includes thousands of DataRefs and commands provided by Laminar Research, which appear with **Vendor** set to _Laminar Research_ and **Aircraft** set to _Generic_.

### DataRefTool

For cases where the HubHop presets do not have what you need, the [DataRefTool plugin](https://datareftool.com/) by Lee Baker provides an interactive way to identify DataRefs and commands as you interact with your aircraft in the virtual cockpit.

**To install DataRefTool:**

1. Download the zip file from the [DataRefTool website](https://datareftool.com/download).
2. Extract the contents to your X-Plane `Resources\Plugins` folder, ensuring the DataRefTool plugin directory contains a `64` folder.
3. Restart X-Plane and load into a flight.
4. Click **Plugins** > **DataRefTool** > **Search** to open the DataRefTool window.

**To find a DataRef or command using DataRefTool:**

Use the buttons in the top-right area of the DataRefTool window to filter the list:

- Click the last button to toggle between showing only DataRefs (**dat**) or only commands (**Cmd**).
- Click the second-to-last button to show only currently changing values (**ch** or **CH**). This lets you interact with the aircraft and see which DataRefs and commands respond to your actions.

You can also filter the list by name using terms like "radio" or "freq" to narrow down the results.

## Configuring MobiFlight for X-Plane

### Reading values from X-Plane

To read a value from X-Plane and display it on a device, use the [X-Plane DataRef](/features/output-variable-types/xplane-dataref/) output variable type in your output configuration.

### Sending commands and writing values to X-Plane

To send a command or write a value to X-Plane in response to a device input, use the [X-Plane (all versions)](/features/input-action-types/x-plane-all-versions/) input action type in your input configuration.

To write a value directly to a DataRef, enable **Show Preset Code**, select **DataRef** from the preset code type dropdown, and enter the DataRef path.

> [!NOTE]
> Not all DataRefs are writable. You can verify whether a DataRef is writable using DataRefTool by selecting the DataRef and checking whether the **Edit** button is available.

## Migrating from XPUIPC

Before the native X-Plane integration, MobiFlight supported X-Plane through XPUIPC, which mirrored FSUIPC's offset-based approach. There is currently no automated migration path from XPUIPC configurations to native X-Plane DataRef and command configurations.

To migrate an XPUIPC configuration:

- **Standard FSUIPC offsets**: Look up the corresponding DataRef or command using DataRefTool, as these offsets are built into XPUIPC and are not listed in a configuration file.
- **Custom offsets in `XpuipcOffsetConfig.cfg`**: Look up the DataRef or command name in your configuration file.

> [!NOTE]
> To continue using XPUIPC instead of migrating, see the [legacy XPUIPC documentation](https://github.com/MobiFlight/MobiFlight-Connector/wiki/X-Plane---Using-XPUIPC-\(DEPRECATED\)).
