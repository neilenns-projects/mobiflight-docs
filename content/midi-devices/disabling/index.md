---
title: Disabling MIDI devices
description: Step-by-step guide for disabling MIDI devices in MobiFlight.
weight: 40
---

<!-- markdownlint-disable MD024 -->
<!-- markdown lint doesn't understand third level headings when used as headings in steps within tabs -->

You may want to disable MobiFlight's MIDI support in certain situations. This can be done either for all MIDI devices or for specific devices. Disabling support is useful when other software controls these devices and MobiFlight should ignore them.

{{< tabs >}}

{{< tab name="Disable all devices" >}}

{{% steps %}}

### Open the Controller Management dialog

Click on the **Extras** menu and select **Controller Management** to open the Controller Management dialog.

{{< screenshot image="/app/extras-controller-management-menu-item.png" title="Screenshot of the Extras menu with the Controller Management menu item selected." >}}

### Disable MIDI device support

On the **Peripherals** tab, uncheck the **Enable MIDI support** checkbox.

{{< screenshot image="disable-all.png" title="Screenshot of the Peripherals tab in Settings with Enable MIDI support unchecked." >}}

{{% /steps %}}

{{< /tab >}}

{{< tab name="Disable specific devices" >}}

{{% steps %}}

### Open the Controller Management dialog

Click on the **Extras** menu and select **Controller Management** to open the Controller Management dialog.

{{< screenshot image="/app/extras-controller-management-menu-item.png" title="Screenshot of the Extras menu with the Controller Management menu item selected." >}}

### Disable specific MIDI devices

On the **Peripherals** tab, uncheck the specific MIDI devices to disable.

{{< screenshot image="disable-specific.png" title="Screenshot of the Peripherals tab in Settings with the MPK mini play device unchecked." >}}

{{% /steps %}}

{{< /tab >}}

{{< /tabs >}}
