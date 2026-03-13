---
title: File types
description: Explanation of the different types of files used by MobiFlight.
---

MobiFlight saves information in several different types of files, depending on their usage.

## MobiFlight projects (.mfproj)

These files contain the input and output configurations that map physical devices to simulator events. They are the primary file used with MobiFlight, and are often uploaded to sites like [flightsim.to](https://flightsim.to/others/mobiflight-profiles/) to share aircraft configurations.

To open a `.mfproj` file, use the **File** > **Open...** menu in the main MobiFlight window.

These files are specific to MobiFlight 11, and replace `.mcc` files from prior releases. They are incompatible with earlier versions of MobiFlight. Any changes made in project files can only be used in MobiFlight 11 or later.

## MobiFlight module configuration (.mfmc)

These files contain the device configuration for a specific board and are saved from the MobiFlight Modules dialog. Typically used to create backups, these files define device-to-board connections without providing simulator event mappings.

## MobiFlight configuration (.mcc)

These files are the legacy format used with MobiFlight 10 and earlier. They contain the input and output configurations that map physical devices to simulator events.

To open a `.mcc` file, use the **File** > **Open...** menu in the main MobiFlight window. MobiFlight 11 will automatically upgrade the file to the new `.mfproj` format.
