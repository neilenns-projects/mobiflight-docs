---
title: MobiFlight - Variable
description: How to use the MobiFlight - Variable input action type with MobiFlight.
weight: 30
---

The **MobiFlight - Variable** action type sets a MobiFlight variable when triggered. This action type is often used to set variables used in pre-conditions for other input configurations, for example when using [a single encoder to tune radio frequencies](/guides/single-encoder-com-tuning/).

{{< screenshot image="mobiflight-variable.png" title="Screenshot of a button input with the MobiFlight - Variable input action type selected." >}}

| Setting | Description                                                                                                                 |
| ------- | --------------------------------------------------------------------------------------------------------------------------- |
| Type    | The type of data stored by the variable, either **Number** or **String**.                                                   |
| Name    | The name for the variable, used when referencing the variable in other configurations.                                      |
| Value   | Specifies the value to set the variable to. Supports value modification with [NCalc](/guides/modifying-values-with-ncalc/). |

> [!TIP]
> To view the current value of a variable, create an output configuration that displays the variable, then look at the **Output Value** column in the main MobiFlight window.
