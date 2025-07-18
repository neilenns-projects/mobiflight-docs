---
title: File types
description: Explanation of the different types of files used by MobiFlight.
---

MobiFlight saves information in several different types of files, depending on their usage.

## MobiFlight configuration (.mcc)

These files contain the input and output configurations that map physical devices to simulator events. They are the primary file used with MobiFlight, and are often uploaded to sites like [flightsim.to](https://flightsim.to/others/mobiflight-profiles/) to share aircraft configurations.

To open a .mcc file, use the **File** > **Open...** menu in the main MobiFlight window.

## MobiFlight module configuration (.mfmc)

These files contain the device configuration for a specific board and are saved from the MobiFlight Modules dialog. Typically used to create backups, these files define device-to-board connections without providing simulator event mappings.

## MobiFlight projects (.mfproj)

These files are specific to the [MobiFlight 11 beta](/guides/mobiflight-eleven/), and replace .mcc files in those releases. They are incompatible with earlier versions of MobiFlight. Any changes made in .mfproj files can only be used in MobiFlight 11 or later.
