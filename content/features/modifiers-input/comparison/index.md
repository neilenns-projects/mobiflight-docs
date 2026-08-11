---
title: Comparison
description: How to use the compare modifier to change input values in MobiFlight.
---

The comparison modifier changes a value based on a boolean logic test of the original value.

The **Operator** dropdown specifies the comparison operator to use. The **Value** field specifies the value to compare against the input value. If the comparison operator returns true, the **Then** value is used. Otherwise, the **Else** value is used.

[NCalc expressions](https://ncalc.github.io/ncalc/articles/index.html) are supported in all three boxes. The current value is represented by the **$** character.

{{< screenshot image="comparison.png" title="Screenshot of an output configuration with the Modify pane open and a compare modifier in edit mode." >}}
