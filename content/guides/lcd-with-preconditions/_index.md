---
title: Showing multiple pages on an LCD
description: Step-by-step guide to using preconditions to show multiple pages of content on an LCD.
ogimage: card-images/devices/lcd-16x2.png
---

MobiFlight preconditions, when combined with two buttons and an LCD, can be used to page between different screens of content on the display. This tutorial demonstrates how to use two buttons to page up and down through two pages, showing COM1 frequencies and COM2 frequencies for a Cessna 172 on an LCD.

> [!NOTE]
> This guide assumes the buttons and LCD are already added as MobiFlight devices following the [button](/devices/button-switch/) and [encoder](/devices/encoder/) guides. It also assumes basic familiarity with creating MobiFlight input configurations.

{{% steps %}}

### Create an input configuration for the page up button

Name the configuration **Page up** and assign the **Device** to the first button. Set the **On Press** action to **MobiFlight - Variable** and the **Name** to **Current LCD page**.

In the **Value** field, enter `($+1)%2`. This will cause the value of the variable to alternate between `0` and `1` on each button press.

{{< screenshot image="input-variable-page-up.png" title="Screenshot of an input configuration mapped to a button, configured as a MobiFlight - Variable action type." >}}

### Create an input configuration for the page down button

Repeat the prior step for the second button, naming the configuration **Page down**. The variable name is the same, **Current LCD page**. The **Value** is `($-1)%2`.

{{< screenshot image="input-variable-page-down.png" title="Screenshot of an input configuration mapped to a button, configured as a MobiFlight - Variable action type." >}}

### Create output configurations for COM frequencies

On the **Output** tab of the main MobiFlight window create entries for each of the four COM frequencies to display:

| Description  | Preset category             | Preset name                   | Index |
| ------------ | --------------------------- | ----------------------------- | ----- |
| COM1 active  | Microsoft / Generic / Radio | `COM ACTIVE FREQUENCY:index`  | 1     |
| COM1 standby | Microsoft / Generic / Radio | `COM STANDBY FREQUENCY:index` | 1     |
| COM2 active  | Microsoft / Generic / Radio | `COM ACTIVE FREQUENCY:index`  | 2     |
| COM2 standby | Microsoft / Generic / Radio | `COM STANDBY FREQUENCY:index` | 2     |

The output configurations are not mapped to any output device. Only the **Sim Variable** tab values need to be set.

> [!TIP]
> For a more in-depth walkthrough of how to display multiple values on an LCD see the [advanced LCD configuration guide](/devices/lcd/advanced-configuration/).

### Create an output configuration to display COM1 frequencies

Create a new output configuration named **COM1 display**. On the **Modify** tab click the **Add reference** button to add references to the **COM1 active** and **COM1 standby** configurations created in the prior step.

{{< screenshot image="com1-config-references.png" title="Screenshot of the output configuration dialog with the Modify tab selected and references added to COM1 active and COM1 standby." >}}

On the **Display** tab use the **Module** and **Use type of** dropdowns to select your connected board and the **LcdDisplay** device type. Select the LCD from the **Display** dropdown.

Format the display output in the **Text** section using the placeholder symbols from the **Modify** tab config references.

{{< screenshot image="com1-display.png" title="Screenshot of the output configuration dialog with the Display tab selected and the Text field filled with COM1: ###.###, STBY: !!!.!!!" >}}

### Add a pre-condition for COM1 display

{{% /steps %}}
