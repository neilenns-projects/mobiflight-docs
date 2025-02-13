---
title: Settings reference
description: Description of all available settings for LCDs and output configurations using LCDs.
ogimage: card-images/devices/lcd.png
weight: 60
---

## Modules dialog

{{< screenshot image="lcd-configuration.png" title="Screenshot of the Modules dialog with the LCD configuration showing." >}}

| Setting | Description                                                                                                                              |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Address | The I^2^C address of the LCD.                                                                                                            |
| Columns | The number of character columns on the LCD. Minimum 1, maximum 40.                                                                       |
| Lines   | The number of rows on the LCD. Minimum 1, maximum 4.                                                                                     |
| Name    | The name for the LCD. Displayed in the output configuration dialog to identify the LCD when mapping the simulator output to the display. |

## Output display configuration

{{< screenshot image="output-configuration.png" title="Screenshot of the Display tab with the LcD output type selected." >}}

| Setting | Description                                                                                                                                                                                                       |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Display | The LCD device configured in the **[Modules dialog](#modules-dialog)** to display the values on.                                                                                                                  |
| Text    | The text to display on the LCD. The **$** character represents digits for the variable configured on the **Sim Variable** tab. Other values can be displayed by defining config references on the **Modify** tab. |
