---
title: Using pre-made MobiFlight profiles
description: Step-by-step instructions for using pre-made WinCtrl profiles with MobiFlight.
prev: /game-controllers/winctrl/
aliases:
  - /joysticks/winwing/premade-profiles/
  - /game-controllers/winwing/premade-profiles/
weight: 10
---

<!-- Markdownlint doesn't understand how ### is used with Hugo shortcodes to show steps in the final markdown -->
<!-- markdownlint-disable MD001 -->

Many MobiFlight profiles for WinCtrl devices are available. See [flightsim.to](https://flightsim.to/discover/winwing) for Microsoft Flight Simulator profiles, and the [X-Plane forums](https://forums.x-plane.org/index.php?/search/&q=winwing&quick=1) for X-Plane profiles.

Take the following steps to use the pre-made profile:

{{% steps %}}

### Extract the downloaded profile

Using **File Explorer**, select the downloaded zip file and click **Extract all** in the ribbon to extract the profile.

> [!TIP]
> Extract the profile to a location other than the Downloads folder. For example, extract to the **Documents\MobiFlight** folder.

{{< screenshot image="file-explorer.png" title="Screenshot of the Windows File Explorer with a downloaded profile zip file selected and the Extract all button highlighted." >}}

### Open the profile in MobiFlight

In the MobiFlight application, go to the **File** menu and select **Open...**.

{{< screenshot image="file-menu.png" title="Screenshot of the MobiFlight main window with the File menu open and the Open...menu item highlighted." >}}

In the resulting file dialog, select the extracted .mcc file, then click **Open**.

{{< screenshot image="file-dialog.png" title="Screenshot of the Windows file dialog with a downloaded .mcc file and the Open button highlighted." >}}

MobiFlight will open the project and automatically map connected WinCtrl controllers to the input and output configurations in the project file.

### View the project configuration

To view the project input and output configurations, click on the `>` button in the project card.

{{< screenshot image="view-project.png" title="Screenshot of the main MobiFlight window with the > button highlighted." >}}

{{% /steps %}}

> [!TIP]
> If MobiFlight is unable to automatically map connected WinCtrl devices to the ones used in the profile, use the **[Controller Bindings](/features/controller-bindings/)** dialog to manually map the devices.

> [!TIP]
> To open multiple profiles at the same time, see the [adding additional profiles](/features/combining-profiles/) to a project documentation.
