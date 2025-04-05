---
title: Modifying values with NCalc
description: How to use NCalc to modify values in MobiFlight.
---

MobiFlight supports NCalc expressions to adjust values received from the simulator. Expressions can be used in:

- Input configurations that have value fields, most commonly **[MobiFlight - Variable](/features/input-action-types/mobiflight-variable/)** configurations.
- [Transform](/features/modifiers/transform/) modifiers on output configurations.
- Value fields in [compare](/features/modifiers/compare/) modifiers on output configurations.

See the [NCalc documentation](https://ncalc.github.io/ncalc/articles/index.html) for a list of supported operators and functions. Several common tasks are accomplished using NCalc. See the following sections for examples.

## Convert a Zulu time in seconds to hours, minutes and seconds (HHMMSS)

Simulators often provide times in number of seconds, but for display it should be formatted as `HH:MM:SS`. Use the [transform](/features/modifiers/transform/) modifier with the following formula:

`Floor($/3600)*10000+Floor($/60)%60*100+$%60`

To display the resulting value with colon separators on an [LCD](/devices/lcd/) use the display string `$$:$$:$$`, where `$` is the matching config variable reference character.

## Cycle between 0 and 1

MobiFlight variables are often used to toggle between `0` and `1` when a button is pressed. Use the following formula as the value for the **On Press** action of the input configuration:

`1-$`

## Cycle between a range of values

MobiFlight variables are often used to store a value within a range. The following formulas, when used as the value field for button input configurations, will increment or decrement the variable value between 0--3 on each press:

| Direction | Formula (with wrapping) | Formula (without wrapping) |
| --------- | ----------------------- | -------------------------- |
| Increment | `if($<3,$+1,0)`         | `if($<3,$+1,3)`            |
| Decrement | `if($>0,$-1,3)`         | `if($>0,$-1,0)`            |

For different ranges, replace `3` with the desired maximum value. The minimum value with the above formulas is always `0`.

## Outputting a string based on a value

MobiFlight supports string values for display on [LCDs](/devices/lcd/). A [transform](/features/modifiers/transform/) modifier with the following formula outputs `ABC` if the simulator variable is `1`; otherwise, it outputs `DEF`:

`if($=1,'ABC','DEF')`

> [!WARNING]
> Use single quotes to enclose the string values, not double quotes.

## Round or truncate values to adjust the decimal precision

Simulator variables often have more digits after the decimal point than required for display. For example, the barometer value has four values after the decimal point when only two are required.

The `Round()` function can be used in a [transform](/features/modifiers/transform/) modifier on an output configuration to adjust the value for display:

`Round($,2)`

The `2` indicates the number of digits to leave after the decimal point. To round the value to the nearest whole number use `Round($,0)`. To truncate the value, instead of rounding, use `Truncate($)` or `Floor($)`.
