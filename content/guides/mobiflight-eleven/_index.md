---
title: MobiFlight 11 preview
description: Using the MobiFlight 11 preview.
ogimage: card-images/guides/mobiflight-eleven.png
---

MobiFlight 11 is a major update to the MobiFlight interface, providing new ways to manage large configuration files. It is currently a preview release, primarily focused on obtaining feedback on the new main window layout.

> [!TIP]
> MobiFlight 11 uses a different file format (.mfproj) than earlier versions of MobiFlight (.mcc). Configuration files from prior versions will get updated automatically when opened, and when saved will be saved in the new format.
>
> Changes made in MobiFlight 11 are not backwards compatible, and MobiFlight 11 files cannot be opened in earlier versions of the application.

## The main window

The main window lists all configurations in the open project. Unlike prior versions, MobiFlight 11 shows input and output configurations in a combined list.

{{< screenshot image="main-window.png" title="Screenshot of the main MobiFlight 11 window with an open project." >}}

The main window shows the following information for each configuration row:

| Name               | Description                                                                                                                                                                         |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Active             | A toggle switch that controls whether the configuration is active. To disable a row, turn off the toggle switch.                                                                    |
| Name / Description | The name and description for the configuration. The sort order can be changed by clicking on {{< icon "switch-vertical" >}} in the column header.                                   |
| Device             | The [device](/devices/), [game controller](/game-controllers/) component, or [MIDI device](/midi-devices/) input assigned to the configuration.                                     |
| Status             | Icons indicating the status for the row. These are not currently implemented, and will always show as disabled.                                                                     |
| Raw Value          | For output configurations, the value received from the simulator before applying any assigned [modifiers](/features/modifiers/). Input configurations will always show **Waiting**. |
| Final Value        | For output configurations, the value for display after applying any assigned [modifiers](/features/modifiers/). Input configurations will always show **Waiting**.                  |

## Adding configurations

To create a new input or output configuration, click the **Add Output Config** or **Add Input Config** button at the bottom of the main window.

{{< screenshot image="main-window-new-config-buttons.png" title="Screenshot of the main window with the Add Output Config and Add Input Config buttons highlighted." >}}

The new configurations will be added in sorted order to the list, named either **New Output Config** or **New Input Config**, depending on the type.

{{< screenshot image="main-window-new-configs-added.png" title="Screenshot of the main window with a New Output Config and New Input Config row." >}}

To rename the configuration, hover over the name and click the {{< icon "pencil-alt" >}} button. Type the new name, then press the enter key to apply the change.

{{< screenshot image="main-window-edit-name.png" title="Screenshot of the main window with the edit name icon for the New Input Config row highlighted." >}}

## Editing configurations

To edit a configuration, click the {{< icon "pencil-alt" >}} button at the far right of the row. This opens the same configuration dialog from prior MobiFlight versions to assign simulator variables, devices, and modifiers.

{{< screenshot image="main-window-edit-config.png" title="Screenshot of the main window with the edit config icon for the New Input Config row highlighted." >}}

## Re-ordering configurations

Rows can be re-ordered by dragging the row using the handle on the left edge of the row.

{{< screenshot image="main-window-reorder-handle.png" title="Screenshot of the main window with the re-order handle on a row highlighted." >}}

## Reverting to the non-beta build

> [!WARNING]
> MobiFlight 11 uses a different file format (.mfproj) than prior versions of MobiFlight.
>
> Changes made to profiles in MobiFlight 11 are not backwards compatible, and cannot be opened in prior versions of MobiFlight after opting out of the beta.

To go back to the non-beta version of MobiFlight, take the following steps.

{{% steps %}}

### Opt out of beta releases

From the **Extras** menu, select **Settings**. Uncheck the **Yes, I would like to receive beta version updates** option, then click **OK** to close the dialog.

{{< screenshot image="beta-version-off.png" title="Screenshot of the settings dialog with the beta version updates checkbox unchecked." >}}

### Uninstall the beta version

Ensure MobiFlight is closed by going to the **File** menu and selecting **Exit**. Then uninstall MobiFlight from the Windows [**Installed apps**](ms-settings:appsfeatures) control panel.

### Install the non-beta version

Install the non-beta version of MobiFlight from the [MobiFlight download page](https://www.mobiflight.com/en/download.html).

{{% /steps %}}
