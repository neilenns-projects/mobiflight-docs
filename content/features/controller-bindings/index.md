---
title: Controller bindings
description: Mapping controllers to profile configurations.
---

MobiFlight projects contain input and output configurations that are bound to physical [boards](/boards/), [game controllers](/game-controllers/), and [MIDI devices](/midi-devices/).

If a connected device is removed, replaced, or has its serial number updated, the project file will no longer be bound to the device. If a device is missing, MobiFlight will attempt to bind to another connected device of the same type.

In situations where MobiFlight fails to automatically re-bind, the **Controller Bindings** dialog allows you to manually update the device bindings.

{{% steps %}}

### Open the Controller Bindings dialog

From the **Extras** menu select **Controller Bindings**.

{{< screenshot image="extras-controller-bindings.png" title="Screenshot of an open project file with the Extras > Controller Bindings menu item highlighted." >}}

### Map the missing device

Each missing device is listed under the **Missing** filter. For each device, use the **Select a controller** dropdown to select a replacement connected device.

{{< screenshot image="select-new-device.png" title="Screenshot of the Controller Bindings dialog with a replacement MobiFlight Mega device highlighted." >}}

### Apply the changes

Click the **Apply changes** button to apply the new device binding to the open profile.

{{< screenshot image="apply-changes.png" title="Screenshot of the Controller Bindings dialog with the Apply changes button highlighted." >}}

### Save the profile

Once the new device binding is applied, save the profile to update the project file so it maintains the new bindings when opening it in the future.

{{< screenshot image="file-save.png" title="Screenshot of an open MobiFlight profile with the File > Save menu highlighted." >}}

{{% /steps %}}
