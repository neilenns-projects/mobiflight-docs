---
title: Showing multiple pages on an LCD
description: Step-by-step guide to using preconditions to show multiple pages of content on an LCD.
ogimage: card-images/guides/multiple-page-lcd.png
---

<!-- markdownlint thinks <none>, which is a value in MobiFlight UI, is inline HTML, so disable the rule in this file. -->
<!-- markdownlint-disable MD033 -->

MobiFlight preconditions, when combined with two buttons and an LCD, can be used to page between different screens of content on the display. This tutorial demonstrates how to use two buttons to page up and down through two pages, showing COM1 frequencies and COM2 frequencies for a Cessna 172 on an LCD.

> [!NOTE]
> This guide assumes the buttons and LCD are already added as MobiFlight devices, following the [button](/devices/button-switch/) and [LCD](/devices/LCD/) guides. It also assumes basic familiarity with creating MobiFlight input and output configurations.

{{% steps %}}

### Create an input configuration for the page up button

Name the configuration **Page up** and assign the **Device** to the first button. Set the **On Press** action to **MobiFlight - Variable** and the **Name** to **Current LCD page**.

In the **Value** field, enter `if($<1,$+1,0)`. This supports two pages, numbered `0` and `1`, and will cycle through the values on each button press.

{{< screenshot image="input-variable-page-up.png" title="Screenshot of an input configuration mapped to a button, configured as a MobiFlight - Variable action type." >}}

> [!TIP]
> To increase the number of display pages, change the first **1** to the desired number of pages minus one. For example, `if($<3,$+1,0)` will support four pages numbered `0`, `1`, `2`, and `3`.

### Create an input configuration for the page down button

Repeat the prior step for the second button, naming the configuration **Page down**. The variable name is the same, **Current LCD page**. The **Value** is `if($>0,$-1,1)`.

{{< screenshot image="input-variable-page-down.png" title="Screenshot of an input configuration mapped to a button, configured as a MobiFlight - Variable action type." >}}

> [!TIP]
> To increase the number of display pages, change **1** to the desired number of pages minus one. For example, `if($>0,$-1,3)` will support four pages numbered `0`, `1`, `2`, and `3`.

### Create output configurations for COM frequencies

On the **Output** tab of the main MobiFlight window, create entries for each of the four COM frequencies to display:

| Description  | Preset category             | Preset name                   | Index |
| ------------ | --------------------------- | ----------------------------- | ----- |
| COM1 active  | Microsoft / Generic / Radio | `COM ACTIVE FREQUENCY:index`  | 1     |
| COM1 standby | Microsoft / Generic / Radio | `COM STANDBY FREQUENCY:index` | 1     |
| COM2 active  | Microsoft / Generic / Radio | `COM ACTIVE FREQUENCY:index`  | 2     |
| COM2 standby | Microsoft / Generic / Radio | `COM STANDBY FREQUENCY:index` | 2     |

The output configurations are not mapped to any output device. Only the **Sim Variable** tab values need to be set.

{{< screenshot image="output-configs.png" title="Screenshot of the output tab of the main MobiFlight window with four output configurations created." >}}

> [!TIP]
> For a more in-depth walkthrough of how to display multiple values on an LCD, see the [advanced LCD configuration guide](/devices/lcd/advanced-configuration/).

### Create an output configuration to display COM1 frequencies

Create a new output configuration named **COM1 display**. On the **Modify** tab, click the **Add reference** button to add references to the **COM1 active** and **COM1 standby** configurations created in the prior step.

{{< screenshot image="com1-config-references.png" title="Screenshot of the output configuration dialog with the Modify tab selected and references added to COM1 active and COM1 standby." >}}

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **LcdDisplay** device type. Select the LCD from the **Display** dropdown.

Format the display output in the **Text** section using the placeholder symbols from the **Modify** tab config references.

{{< screenshot image="com1-display.png" title="Screenshot of the output configuration dialog with the Display tab selected and the Text field filled with COM1: ###.###, STBY: !!!.!!!." >}}

### Add a precondition for COM1 display

<!-- markdownlint-disable-next-line MD033 -->

On the **Precondition** tab for the **COM1 display** config, click on **<none>** and change **Use type of** to **MobiFlight Variable**.

The **Current LCD page** variable created earlier should automatically be selected in the **Choose variable** dropdown. Use `0` for the **If current value is** comparison.

This will ensure the **COM1 display** output configuration is only active when the **Current LCD page** variable is set to `0`.

{{< screenshot image="com1-precondition.png" title="Screenshot of the Precondition tab with the Current LCD page variable selected and the precondition set to = 0." >}}

### Create an output configuration to display COM2 frequencies

Create a new output configuration named **COM2 display**. On the **Modify** tab, click the **Add reference** button to add references to the **COM2 active** and **COM2 standby** configurations created in the prior step.

{{< screenshot image="com2-config-references.png" title="Screenshot of the output configuration dialog with the Modify tab selected and references added to COM2 active and COM2 standby." >}}

On the **Display** tab, use the **Module** and **Use type of** dropdowns to select your connected board and the **LcdDisplay** device type. Select the LCD from the **Display** dropdown.

Format the display output in the **Text** section using the placeholder symbols from the **Modify** tab config references.

{{< screenshot image="com2-display.png" title="Screenshot of the output configuration dialog with the Display tab selected and the Text field filled with COM2: ###.###, STBY: !!!.!!!." >}}

### Add a precondition for COM2 display

On the **Precondition** tab for the **COM2 display** config, click on **<none>** and change **Use type of** to **MobiFlight Variable**.

The **Current LCD page** variable created earlier should automatically be selected in the **Choose variable** dropdown. Use `1` for the **If current value is** comparison.

This will ensure the **COM2 display** output configuration is only active when the **Current LCD page** variable is set to `1`.

{{< screenshot image="com2-precondition.png" title="Screenshot of the Precondition tab with the Current LCD page variable selected and the precondition set to = 1." >}}

### Try it out

Spawn an airplane in Microsoft Flight Simulator. Make sure the MobiFlight **Run** button is clicked in the toolbar. The LCD should display the active and standby frequencies for COM1. Pressing the **Page up** and **Page down** buttons should cycle through the COM1 and COM2 display pages.

MobiFlight will indicate which output configuration is disabled by the precondition by showing a red exclamation point at the start of the row. In the following screenshot, **COM1 display** is active and **COM2 display** is disabled.

{{< screenshot image="com2-disabled.png" title="Screenshot of the main MobiFlight window output tab with a red exclamation mark next to the COM2 display row." >}}

{{% /steps %}}
