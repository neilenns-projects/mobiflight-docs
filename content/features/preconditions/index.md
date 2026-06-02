---
title: Preconditions
description: Overview of preconditions in MobiFlight configs.
---

Preconditions control whether an input or output config is active based on a value. They are an advanced feature, and are best understood by following existing guides for common use cases:

- [Using a single encoder to tune COM1](/guides/single-encoder-com-tuning) demonstrates using preconditions on input configurations.
- [Using the selector knob on a Honeycomb Bravo](/guides/honeycomb-bravo-selector-knob/) demonstrates using preconditions on input configurations with a game controller.
- [Showing multiple display pages on an LCD](/guides/multiple-page-lcd/) demonstrates using preconditions on output configurations.

The following sections provide reference information for the features of the precondition tab.

## Adding a precondition

Preconditions are added to configurations using the **Precondition** tab. By default a single precondition is shown with no
active rules. To add additional preconditions, right-click in the precondition list and select **Add Precondition** from the context menu.

{{< screenshot image="add-precondition.png" title="Screenshot of a precondition with the context menu open and the Add Precondition menu item highlighted." >}}

## Editing a precondition

Every precondition has settings that define when the configuration should be active. To edit the settings, click on the precondition in the list, then use the **Precondition type** section to define the condition rules.

{{< screenshot image="mhz-precondition.png" title="Screenshot of the precondition tab with the COM1 KHz mode variable selected and the precondition set to = 0." >}}

**MobiFlight Variable** is the most common type, and uses the value of a MobiFlight variable in the condition test. Select the variable from the dropdown, then define the logical operator and value to test against.

**Config item** uses the value of a config reference defined on the **Config References** tab as the value for the condition test.

## Changing the logic operator

When multiple preconditions are defined on a single config, logical operators indicate how the conditions should combine. By default each condition is added as an `AND` condition. To change the condition to an `OR` condition, right-click on it and select **Logical Operator** from the context menu.

{{< screenshot image="logical-operators.png" title="Screenshot of a precondition with the context menu open to the Logical Operators menu item." >}}

## Removing a precondition

To remove a precondition, right-click on the precondition and select **Remove Precondition** from the context menu.

{{< screenshot image="remove-precondition.png" title="Screenshot of a precondition with the context menu open and the Remove Precondition menu item highlighted." >}}
