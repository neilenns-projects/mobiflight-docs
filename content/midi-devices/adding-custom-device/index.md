---
title: Custom MIDI devices
description: Step-by-step guide for adding custom MIDI devices in MobiFlight.
weight: 50
---

MIDI devices other than the ones supported by MobiFlight can be added by creating a configuration file that defines how to map **Note** and **CC** messages.

{{% steps %}}

### Enable logging

Follow the steps in the [sharing logs guide](/guides/sharing-logs) to enable **Info** logging in MobiFlight.

### Identify Note and CC for each input

Launch MobiFlight and take note of the **Midi device** name reported when the device is detected.

Then, use each input on the board and take note of the name, **Note** and **CC** values received by MobiFlight.

{{< screenshot image="logs.png" title="Screenshot of the MobiFlight main window with logging enabled. The MPK mini play, Note 1_65, and CC 1_50 log entries are highlighted." >}}

For example, the following log entry indicates a **Note** message type on channel **1** with **MessageId** 15:

`
02/28/2025 14:33:15(659): Razer Stream Controller => Note 1_15  => PRESS =>  No config found.
`

### Create the configuration file

Create a new text file ending with `.midiboard.json` and save it in the `%LOCALAPPDATA%\MobiFlight\MobiFlight Connector\MidiBoards` folder.

Using the [`mpd218.midiboard.json`](https://github.com/MobiFlight/MobiFlight-Connector/blob/main/MidiBoards/mpd218.midiboard.json) file as an example, create a new configuration file using the values identified in the previous step.

Make sure to set `InstanceName` to the **Midi device** name detected by MobiFlight at launch.

> [!TIP]
> Using an editor like [Visual Studio Code](https://code.visualstudio.com/download) will provide syntax highlighting and validation the configuration files.

### Verify the configuration

Launch MobiFlight and create a new input configuration. Verify the inputs on the MIDI device are displayed correctly in the **Device** dropdown.

{{% /steps %}}
