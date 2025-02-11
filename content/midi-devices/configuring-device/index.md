---
title: Configuring the device
description: Step-by-step guide for configuring MIDI devices for use in MobiFlight.
toc: false
prev: /midi-devices/
weight: 10
---

<!-- markdownlint-disable MD024 -->
<!-- markdown lint doesn't understand third level headings when used as headings in steps within detail sections -->

Most MIDI devices require configuration with a vendor-provided application before use with MobiFlight. See the section below for instructions on how to configure your specific device.

{{% details title="AKAI MDP218" closed="true" %}}

The AKAI MPD218 must be configured using the [MPD218 editor](https://cdn.inmusicbrands.com/akai/attachments/MPD218/MPD218_Editor_v1.0.8.exe)

{{% steps %}}

### Set the default configuration

All pad banks should be set to the **Note** type. The note ranges are:

- **36--51**
- **52--67**
- **68--83**

Knobs should be set to the **CC** type. The ranges are:

- **[3, 9, 12, 13, 14, 15]**
- **16--21**
- **22--27**

{{< screenshot image="akai-mpd218/default-configuration.png" title="Screenshot of the MPD218 editor with the default configuration applied." >}}

### Change the knob configuration

From the **File** menu, select **Load From Hardware**. Set the knob **TYPE** to **INC/DEC 2**. Save the changes by selecting **Save To Hardware** from the **File** menu.

{{< screenshot image="akai-mpd218/knob-type.png" title="Screenshot of the MPD218 editor with the knob type changed to INC/DEC 2." >}}

{{% /steps %}}

{{% /details %}}

{{% details title="AKAI MPK mini play" closed="true" %}}

The Akai MPK mini play works without additional configuration. For proper operation, ensure the standard octave is selected.

{{% /details %}}

{{% details title="Behringer X-TOUCH MINI" closed="true" %}}

The Behringer X-TOUCH MINI must be configured using the [Behringer X-Touch Editor (direct download)](https://mediadl.musictribe.com/download/software/behringer/X-TOUCH/X-TOUCH-EDITORv1-21.zip)

{{% steps %}}

### Configure the faders

Faders must be set to the **CC** type.

{{< screenshot image="behringer-x-touch-mini/faders.png" title="Screenshot of the Behringer X-Touch Editor with the fader type set to CC." >}}

### Configure the buttons

Buttons must be set to the **Note** type.

{{< screenshot image="behringer-x-touch-mini/buttons.png" title="Screenshot of the Behringer X-Touch Editor with the button type set to Note." >}}

### Configure the encoders

Encoders must be set to the **CC** type.

{{< screenshot image="behringer-x-touch-mini/encoders.png" title="Screenshot of the Behringer X-Touch Editor with the encoder type set to CC." >}}

### Set the global channel

The **Global Channel** must be set to **1**.

{{% /steps %}}

{{% /details %}}

{{% details title="Intech EF44" closed="true" %}}

The Intech EF44 must be configured using the [Grid Editor](https://intech.studio/support-and-downloads#editor-software). Use the {{< a href="MobiFlight-ef44-profile.json" download="MobiFlight-ef44-profile" >}}pre-defined MobiFlight session profile{{< /a >}} and load it in the Grid Editor.

{{% /details %}}

{{% details title="KORG nanoKONTROL 2" closed="true" %}}

The KORG nanoKONTROL2 must be configured using the [KORG KONTROL Editor](https://www.korg.com/us/support/download/software/0/159/1354/)

{{% steps %}}

### Assign CC numbers

CC numbers must be assigned as shown in the following screenshot.

{{< screenshot image="korg-nanokontrol-2/cc-numbers.png" title="Screenshot of the KORG KONTROL Editor with the default CC numbers applied." >}}

### Enable knobs and sliders

All knobs and sliders must be enabled.

### Configure the buttons

All buttons must have their **Type** set to **Control Change**. The **Button Behavior** must be set to **Momentary** and the **Off Value** set to **0**.

### Configure the LEDs

Read the current configuration by going to **Communication**, then **Receive Scene Data**.

Select the **Control** tab then the **Common** group and change **LED Mode** to **External**.

Save the configuration by going to **Communication**, then **Write Scene Data**.

{{< screenshot image="korg-nanokontrol-2/led-mode.png" title="Screenshot of the KORG KONTROL Editor with the LED mode set to External." >}}

{{% /steps %}}

{{% /details %}}
