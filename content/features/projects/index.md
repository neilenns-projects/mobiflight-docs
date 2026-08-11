---
title: Projects
description: Overview of MobiFlight projects.
---

MobiFlight projects (.mfproj) are the core files that define the input and output configurations for your MobiFlight setup, and connect those configurations to physical hardware. Each project contains one or more [profiles](/features/profiles/) that map the physical hardware to simulator events.

## Creating projects

{{% steps %}}

### Start a new project

Select **New** from the **File** menu.

{{< screenshot image="file-new.png" title="Screenshot of the main MobiFlight window with the File > New menu highlighted." >}}

### Provide the project settings

In the **Project Name** field specify a name for the project. This is typically the name of the aircraft the project will be used with, for example **Cessna 172**.

{{< screenshot image="project-name.png" title="Screenshot of the new project dialog with Cessna 172 entered as the project name and highlighted." >}}

Then, select the flight simulator the project will be used with. Selecting the correct simulator when creating the project ensures input and output configurations will display the correct list of simulator events.

{{< screenshot image="simulator.png" title="Screenshot of the new project dialog with Microsoft Flight Simulator button selected and highlighted." >}}

Optionally, enable additional features. For Microsoft Flight Simulator projects targeting PMDG aircraft, check the **FSUIPC** option. For projects targeting ProSim aircraft, check the **ProSim** option.

> [!TIP]
> The FSUIPC option is only required for profiles targeting PMDG aircraft.

### Specify the aircraft type

MobiFlight filters the available simulator events in input and output configs by the aircraft specified in the project. By default only `Microsoft Generic` events are displayed. To add additional aircraft to the event list click the edit button.

{{< screenshot image="edit-aircraft.png" title="Screenshot of the new project dialog with aircraft edit button highlighted." >}}

Then, use the aircraft pane to filter for the aircraft.

{{< screenshot image="filter-aircraft.png" title="Screenshot of the aircraft pane with the list filtered by Cessna 172." >}}

Finally, select the appropriate aircraft then click **Go Back**.

{{< screenshot image="select-aircraft.png" title="Screenshot of the aircraft pane with Cessna 172 selected." >}}

### Create the project

Click the **Create project** button to create the project and open the project editor.

{{< screenshot image="create-project.png" title="Screenshot of the new project dialog with the Create project button highlighted." >}}

### Save the project

After creating the project, save it by selecting **Save** from the **File** menu.

{{< screenshot image="file-save.png" title="Screenshot of the main MobiFlight window with the File > Save menu highlighted." >}}

Give the project file a name in a meaningful location, such as a **MobiFlight Projects** folder inside your **Documents** folder, then click the **Save** button to save the new project.

{{< screenshot image="file-save-dialog.png" title="Screenshot of the file save dialog with the filename set to Cessna 172 and highlighted." >}}

{{% /steps %}}

## Opening an existing project

{{% steps %}}

### Open the project in MobiFlight

In MobiFlight, go to the **File** menu and select **Open...**.

{{< screenshot image="file-menu.png" title="Screenshot of the MobiFlight main window with the File menu open and the Open...menu item highlighted." >}}

In the resulting file dialog, select the .mfproj file for the project you want to open and click **Open**.

{{< screenshot image="file-dialog.png" title="Screenshot of the Windows file dialog with a downloaded .mfproj file and the Open button highlighted." >}}

{{% /steps %}}

## Merging profiles from other projects

Profiles from multiple projects can be merged, creating a single project containing all the inputs and outputs from the separate files. This is particularly useful when downloading pre-made profiles for specific hardware devices.

{{% steps %}}

### Open the primary project

Open the primary project that the other profiles will merge into, using the **Open** item in the **File** menu or by clicking on the `>` in the recent projects list.

{{< screenshot image="open-primary-project.png" title="Screenshot of the main MobiFlight window with > highlighted on a recent project." >}}

### Add additional profiles

Select the **From existing project** item from the **+** menu in the tab bar.

{{< screenshot image="plus-menu.png" title="Screenshot of an open profile with the + menu highlighted." >}}

Navigate to the project that contains the profiles to merge and click **Open**.

{{< screenshot image="file-open-additional-profile.png" title="Screenshot of a file open dialog with a project and the Open button highlighted." >}}

The selected project will have its profiles merged with the currently open project, and the profiles will show as additional tabs.

{{< screenshot image="merged-tab.png" title="Screenshot of an open MobiFlight project with an additional profile tab highlighted." >}}

Use the **Save** item in the **File** menu to save the changes to the primary project.
{{% /steps %}}

> [!IMPORTANT]
> These steps **merge** the secondary files into the primary file. To make modifications to the configurations in the secondary files, be sure to edit the primary file after merging.
>
> Changes to the secondary files will not automatically appear in the primary file.

## Removing a project from recent projects

To remove a project from the recent projects list, click the trash can icon.

{{< screenshot image="remove-from-recent.png" title="Screenshot of the MobiFlight main window with the trash can icon highlighted on a recent project." >}}

> [!TIP]
> This only removes the project from the recent projects list. It does not delete the project from your computer.

## Editing project settings

To edit the settings on an existing project, for example to change the aircraft in the project, click the **...** menu next to the project name and select **Settings**.

{{< screenshot image="project-settings-menu.png" title="Screenshot of the MobiFlight main window with the project menu opened and the Settings item highlighted." >}}

## Renaming a project

To rename a project, click the **...** menu next to the project name and select **Rename**.

{{< screenshot image="project-rename-menu.png" title="Screenshot of the MobiFlight main window with the project menu opened and the Rename item highlighted." >}}

Then, type a new project name and press **Enter** to apply the change.

{{< screenshot image="renamed-project.png" title="Screenshot of the MobiFlight main window with the project name edited to Cessna 172 (2024)." >}}

> [!IMPORTANT]
> Renaming a project only changes the name of the project shown in the MobiFlight tab. It does not change the filename of the `.mfproj` file saved on your computer.
