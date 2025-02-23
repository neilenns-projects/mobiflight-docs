---
title: Modifiers
description: How to use modifiers to change output values in MobiFlight.
next: /guides/modifiers/blink/
---

Modifiers provide a way to adjust values received from the simulator before they are displayed on an output [device](/devices/). The following modifiers are supported:

- [Blink](blink/)
- [Compare](compare/)
- [Interpolation](interpolation/)
- [Padding](padding/)
- [Substring](substring/)
- [Transform](transform/)

## Adding a modifier

Modifiers are added to output configurations using the **Modify** tab. Click the **Add Modifier** button, then select the modifier to add.

{{< screenshot image="add-modifier.png" title="Screenshot of an output configuration with the Modify tab selected and the Add Modifier menu button open." >}}

## Editing modifier settings

Every modifier has settings that control how the output value is changed. To edit modifier settings, click on the modifier in the dialog to expand the options.

{{< screenshot image="edit-modifier.png" title="Screenshot of an output configuration with the Modify tab selected and a Comparison modifier highlighted." >}}

## Managing multiple modifiers

Output configurations can have multiple modifiers assigned. Modifiers are processed in order, from top to bottom, with the modifier result passed to the next modifier in the list.

To re-order the modifiers use the up and down arrows. To disable an individual modifier, uncheck the **use** checkbox next to the modifier name.

{{< screenshot image="multiple-modifiers.png" title="Screenshot of an output configuration with the Modify tab selected, and the substring and padding modifiers added." >}}

## Removing a modifier

To remove a modifier click the **X** button on the modifier row.

{{< screenshot image="remove-modifier.png" title="Screenshot of an output configuration with the Modify tab selected, and the substring and padding modifiers added. The X button for the Substring modifier is highlighted." >}}
