---
title: Modifiers - input configs
description: How to use modifiers to change input values in MobiFlight.
next: /features/modifiers-input/blink/
---

Modifiers provide a way to adjust input values from a [device](/devices/) before they are used in a simulator event. The following modifiers are supported:

- [Blink](/features/modifiers-input/blink/)
- [Comparison](/features/modifiers-input/comparison/)
- [Interpolation](/features/modifiers-input/interpolation/)
- [Padding](/features/modifiers-input/padding/)
- [Substring](/features/modifiers-input/substring/)
- [Transformation](/features/modifiers-input/transformation/)

## Adding a modifier

Modifiers are added to input configurations using the **Modifiers** button. Click the **Modifiers**, then click the **Add modifier** button and select the modifier type.

{{< screenshot image="add-modifier.png" title="Screenshot of an input configuration with the Modify pane open and the Add Modifier menu button open." >}}

## Editing modifier settings

Every modifier has settings that control how the input value is changed. To edit modifier settings, click the expand arrow next to the modifier in the **Modifiers** pane to expand the options.

{{< screenshot image="edit-modifier.png" title="Screenshot of an input configuration with the Modify pane open and a Transformation modifier highlighted." >}}

## Re-ordering modifiers

Input configurations can have multiple modifiers assigned. Modifiers are processed in order, from top to bottom, with the modifier result passed to the next modifier in the list.

To re-order the modifiers, use the up and down arrows.

{{< screenshot image="reorder-modifier.png" title="Screenshot of an input configuration with the Modify pane open, two modifiers listed, and the re-ordering arrows highlighted." >}}

## Disabling a modifier

To disable a modifier, use the toggle switch on the modifier.

{{< screenshot image="disable-modifier.png" title="Screenshot of the Modifiers pane with the toggle switch highlighted." >}}

## Removing a modifier

To remove a modifier, click the delete icon next to the modifier.

{{< screenshot image="remove-modifier.png" title="Screenshot of the Modifiers pane with a delete icon highlighted." >}}
