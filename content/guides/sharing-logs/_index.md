---
title: Sharing logs
description: How to share logs from MobiFlight when requesting support.
---

MobiFlight logs make it easier for people to answer support questions in [Discord](https://discord.gg/yUaBqMbz). The following steps show how to enable and share logs from MobiFlight.

> [!IMPORTANT]
> Always share the complete log file using these steps when requested. Sharing partial logs, or screenshots of logs,
> delays support and makes it harder to resolve questions.

{{% steps %}}

### Re-create the issue

Re-create the issue. Depending on the problem, this may include:

- Closing and running MobiFlight.
- Attempting to update the board firmware.
- Interacting with devices.
- Triggering events in the simulator.

### Copy the logs to the clipboard

After re-creating the issue, copy the logs to the clipboard by going to the **Extras** menu and selecting **Copy logs to clipboard**. A success dialog will show after the logs are copied.

{{< screenshot image="extras-copy-logs.png" title="Screenshot of the Extras menu with the Copy logs to clipboard menu item selected." >}}

### Paste the logs in Discord

Switch to Discord and click in the message box for the support thread, then press **CTRL+V** to paste the logs. Discord will automatically convert the logs to a text attachment.

{{< screenshot image="discord-logs-pasted.png" title="Screenshot of Discord with the logs pasted as a message.txt attachment." >}}

{{% /steps %}}

## Changing the log level

In some instances you may be asked to adjust the log level to ensure additional debugging information is captured. To adjust the log level:

{{% steps %}}

### Open the settings dialog

Click on the **Extras** menu and select **Settings** to open the settings dialog.

{{< screenshot image="/app/extras-settings-menu-item.png" title="Screenshot of the Extras menu with the Settings menu item selected." >}}

### Change the log level

Set the **Log Level** dropdown to the requested level, then click **Save** to apply the change.

{{< screenshot image="settings-log-level.png" title="Screenshot of the Settings dialog with the Log Level dropdown open and highlighted." >}}

> [!IMPORTANT]
> After the issue is resolved, set the log level back to **Info**.

{{% /steps %}}
