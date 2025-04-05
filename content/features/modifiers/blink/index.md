---
title: Blink
description: How to use the blink modifier to change output values in MobiFlight.
aliases:
  - /guides/modifiers/blink/
---

The blink modifier alternates the output value between **0** and **1** when the original value is **1**.

The **Blink value** dropdown specifies what value should be sent when the blink sequence is in the **1** state. It can either be **0**, **1**, **Space**, or a custom character.

The **Blink sequence** specifies how many milliseconds the value should be **On** followed by how many milliseconds the value should be **Off**. Multiple sequences can be added using the **Add** button to create complex blink patterns.

{{< screenshot image="blink.png" title="Screenshot of an output configuration with the Modify tab selected and a blink modifier in edit mode." >}}
