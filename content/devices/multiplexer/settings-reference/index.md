---
title: Settings reference
description: Description of all available settings for multiplexer devices and input configurations using multiplexers.
ogimage: card-images/devices/multiplexer.png
weight: 40
---

## Modules dialog

{{< screenshot image="multiplexer-configuration.png" title="Screenshot of the Modules dialog with the multiplexer configuration showing." >}}

| Setting | Description                                                                                                                                                                 |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| S0      | The board pin connected to the S0 pin of the multiplexer. All digital and analog pins are supported. This pin is shared by all multiplexers connected to the board.         |
| S1      | The board pin connected to the S1 pin of the multiplexer. All digital and analog pins are supported. This pin is shared by all multiplexers connected to the board.         |
| S2      | The board pin connected to the S2 pin of the multiplexer. All digital and analog pins are supported. This pin is shared by all multiplexers connected to the board.         |
| S3      | The board pin connected to the S3 pin of the multiplexer. All digital and analog pins are supported. This pin is shared by all multiplexers connected to the board.         |
| Data    | The board pin connected to the data pin of the multiplexer. All digital and analog pins are supported. This pin must be unique for each multiplexer connected to the board. |
| Type    | The type of multiplexer connected, either **8-bit multiplexer** or **16-bit multiplexer**.                                                                                  |
| Name    | The name for the multiplexer. Displayed in the input configuration dialog to identify the multiplexer when mapping the input to a simulator event.                          |

## Input configuration

Multiplexers have the same input setting events as [buttons and switches](/devices/button-switch/settings-reference/#input-configuration).

Use the **Device** dropdowns to select the multiplexer and specific input on the multiplexer to use.

{{< screenshot image="input-configuration.png" title="Screenshot of the input configuration wizard for a multiplexer, with the Multiplexer and input 0 selected." >}}
