---
title: Blink
description: How to use the blink modifier to change input values in MobiFlight.
---

The blink modifier alternates the output value between the specified **Alternate value** (typically `0`) when the original value is `0` and `1` when the original value is `1`.

The **Alternate value** field specifies what value should be sent when the blink sequence is in the **0** state.

The **Blink sequence** specifies how many milliseconds the value should be **On** followed by how many milliseconds the value should be **Off**. Multiple sequences can be added using the **Add blink interval** button to create complex blink patterns.

{{< screenshot image="blink.png" title="Screenshot of an input configuration with the Modify pane open and a blink modifier in edit mode." >}}
