---
title: Using pre-made MobiFlight profiles
description: Step-by-step instructions for using pre-made WINWING profiles with MobiFlight.
aliases:
  - /joysticks/winwing/premade-profiles/
weight: 10
---

Many MobiFlight profiles for WINWING devices are available. See [flightsim.to](https://flightsim.to/discover/winwing) for Microsoft Flight Simulator profiles, and the [X-Plane forums](https://forums.x-plane.org/index.php?/search/&q=winwing&quick=1) for X-Plane profiles.

Take the following steps to use the pre-made profile:

{{% steps %}}

### Extract the downloaded profile

Using **File Explorer**, select the downloaded zip file and click **Extract all** in the ribbon to extract the profile.

{{< screenshot image="file-explorer.png" title="Screenshot of the Windows File Explorer with a downloaded profile zip file selected and the Extract all button highlighted." >}}

### Open the profile in MobiFlight

In the MobiFlight application, go to the **File** menu and select **Open...**.

{{< screenshot image="file-menu.png" title="Screenshot of the MobiFlight main window with the File menu open and the Open...menu item highlighted." >}}

In the resulting file dialog, select the extracted .mcc file, then click **Open**.

{{< screenshot image="file-dialog.png" title="Screenshot of the Windows file dialog with a downloaded .mcc file and the Open button highlighted." >}}

### Acknowledge the orphaned device warning

When the profile is opened in MobiFlight, the following warning dialog will show. Click **Ok**.

{{< screenshot image="orphaned-warning.png" title="Screenshot of the orphaned device warning dialog indicating the WINWING joystick in the profile is not found." >}}

### Map the missing WINWING device to an available device

After clicking **OK** in the previous step, MobiFlight displays a dialog to map the missing device to an available device.

Select the missing WINWING device in the **Select an orphaned serial** list, then select the correct WINWING device to use instead from the **Select a connected module and assign** dropdown.

{{< screenshot image="orphaned-serial-dialog.png" title="Screenshot of the orphaned serials dialog with an orphaned WINWING device highlighted in red, and the appropriate replacement device highlighted in red." >}}

After selecting the WINWING joystick to use, click the **Assign** button.

### Save the updated profile

Confirm the mapped WINWING joystick works correctly with the profile, then select **Save** from the main window toolbar to ensure the downloaded profile maintains the new joystick mapping.

{{% /steps %}}
