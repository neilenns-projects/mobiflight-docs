---
title: Auto-loading configurations
description: How to automatically load a configurations when an aircraft spawns.
---

MobiFlight supports linking configuration files with specific aircraft. Linked configurations can be automatically loaded when the associated aircraft is spawned in the simulator.

## Linking a profile

To link a profile to an aircraft do the following steps:

{{% steps %}}

### Spawn the aircraft to link

Launch the flight simulator and spawn the aircraft.

### Open the configuration file

Open the appropriate configuration file using the **File** > **Open...** menu item.

### Link the configuration file

Select the down arrow next to the aircraft name in the main window status bar and click **Link current config**.

{{< screenshot image="link-current-config.png" title="Screenshot of the main MobiFlight window with the aircraft menu open and the Link current config menu item highlighted." >}}

{{% /steps %}}

The aircraft name will show a green checkmark next to it when the open configuration file is linked to the active aircraft.

> [!TIP]
> Liveries are considered a separate aircraft and must be individually linked to the appropriate configuration.

## Unlinking a profile

To remove the link between a profile and an aircraft do the following steps:

{{% steps %}}

### Spawn the aircraft to unlink

Launch the flight simulator and spawn the aircraft.

### Remove the link

Select the down arrow next to the aircraft in the main window status bar, and click **Remove link**.

{{< screenshot image="remove-link.png" title="Screenshot of the main MobiFlight window with the aircraft menu open and the Remove link menu item highlighted." >}}

{{% /steps %}}

## Enabling auto-load

To enable automatic configuration loading, after linking a configuration with an aircraft, select the down arrow next to the aircraft name in the main window status bar, and check the **Auto-load linked config** menu item.

{{< screenshot image="auto-load-linked-config-checked.png" title="Screenshot of the main MobiFlight window with the aircraft menu open and the Auto-load linked config menu item checked and highlighted." >}}

## Disabling auto-load

To disable automatic configuration loading, select the down arrow next to the aircraft name in the main window status bar, and uncheck the **Auto-load linked config** menu item.

{{< screenshot image="auto-load-linked-config-unchecked.png" title="Screenshot of the main MobiFlight window with the aircraft menu open and the Auto-load linked config menu item unchecked and highlighted." >}}
