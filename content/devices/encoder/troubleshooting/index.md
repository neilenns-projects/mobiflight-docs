---
title: Troubleshooting
description: Troubleshooting encoder issues.
ogimage: card-images/devices/encoder-both.png
weight: 40
---

While most rotary encoders work the same, there can be subtle differences.
It is important that your encoder type is set properly, or your encoders
will not register the inputs correctly.

{{% steps %}}

### Enable logging

Follow the [logging guide](/guides/sharing-logs/) to enable info logging.

### Rotate the encoder knob

Turn the encoder knob left and right. You should see exactly one **LEFT** or **RIGHT**
event per click, and your log should match the direction you are turning.

### Adjust the type

If you need two clicks to see one event on the log, change the encoder type to
`2 detents per cycle (00, 11)`. If it takes four clicks to see one event, use
`4 detents per cycle`.

> [!TIP]
> There is no need to close the dialog when you are testing different encoder types.
> Select a new type and click **Upload config**, and you can see the results in the
> log immediately.

### Direction change

If you get missed clicks, or you get events in the wrong direction when you turn
the knob in the other direction, use the other variant with the same number of detents.

If everything works exactly right, congratulations! Don't forget to *Upload config* 
so your correct setting is saved!

{{% /steps %}}
