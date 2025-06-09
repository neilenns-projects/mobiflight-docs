---
title: File types
description: Explanation of the different types of files used by MobiFlight.
---

MobiFlight saves information in several different types of files, depending on their usage.

## MobiFlight configuration (.mcc)

These files contain the input and output configurations that map physical devices to simulator events. They are the primary file used with MobiFlight, and are often uploaded to sites like [flightsim.to](https://flightsim.to/others/mobiflight-profiles/) to share aircraft configurations.

To open a .mcc file, use the **File** > **Open...** menu in the main MobiFlight window.

## MobiFlight module configuration (.mfmc)

These files contain the device configuration for a specific board. They are saved from the MobiFlight Modules dialog, and are typically used to create backups of board configurations. They do not provide mappings of the devices to simulator events. They only define how devices are connected to a board.

## MobiFlight projects (.mfproj)

These files are specific to the [MobiFlight 11 beta](/guides/mobiflight-eleven/), and replace .mcc files in those releases. They are not compatible with earlier versions of MobiFlight. Any changes made in .mfproj files can only be used in MobiFlight 11 or later.
