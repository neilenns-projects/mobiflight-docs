---
title: Disabling game controllers
description: Step-by-step guide for disabling game controllers in MobiFlight.
aliases:
  - /joysticks/disabling/
weight: 40
---

<!-- markdownlint-disable MD024 -->
<!-- markdown lint doesn't understand third level headings when used as headings in steps within tabs -->

You may want to disable MobiFlight's game controller support in certain situations. This can be done either for all game controllers or for specific devices. Disabling game controller support is useful when other software controls these devices, and MobiFlight should ignore them.

{{< tabs items="Disable all game controllers,Disable specific game controllers" >}}

{{< tab >}}

{{% steps %}}

### Open the settings dialog

Go to the **Extras** menu and select **Settings**.

{{< screenshot image="/extras-settings.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

### Disable joystick support

On the **Peripherals** tab, uncheck the **Enable joystick support** checkbox.

{{< screenshot image="disable-all.png" title="Screenshot of the Peripherals tab in Settings with Enable joystick support unchecked." >}}

{{% /steps %}}

{{< /tab >}}

{{< tab >}}

{{% steps %}}

### Open the settings dialog

Go to the **Extras** menu and select **Settings**.

{{< screenshot image="/extras-settings.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

### Disable specific game controllers

On the **Peripherals** tab, uncheck the specific game controller to disable.

{{< screenshot image="disable-specific.png" title="Screenshot of the Peripherals tab in Settings with three FootSwitch game controllers disabled." >}}

{{% /steps %}}

{{< /tab >}}

{{< /tabs >}}
