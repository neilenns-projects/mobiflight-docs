---
title: Advanced workshop
description: Step-by-step guide to configuring the advanced workshop project with MobiFlight.
ogimage: card-images/guides/workshop-advanced.png
weight: 30
---

The advanced workshop builds a panel that includes push buttons, an LCD, and a dual encoder, to scroll through COM1 and COM2 active and standby frequencies, and to change the MHz and KHz components of the standby frequencies.

## Required components

The following components are required for the project:

| Part                                                                                        | Quantity |
| ------------------------------------------------------------------------------------------- | -------- |
| [Mega 2560 Pro Mini](https://shop.mobiflight.com/product/arduino-mega-2560-pro-mini-usb-c)  | 1        |
| [MobiFlight prototyping board](https://shop.mobiflight.com/product/prototyping-board-v2)    | 1        |
| [Enclosure](#3d-printed-enclosure-parts)                                                    | 1        |
| [LED push button](/devices/button-switch/)                                                  | 2        |
| [Dual encoder with breakout board](https://shop.mobiflight.com/product/dual-encoder-bundle) | 1        |
| Micro-switch PCB                                                                            | 1        |
| XH-JST 3-pin wire                                                                           | 1        |
| XH-JST 4-pin wire                                                                           | 3        |
| M3x5mm screw                                                                                | 12       |

## 3D-printed enclosure parts

The following parts make up the 3D-printed enclosure:

- [Base](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/advanced/stl/workshop-advanced-base.stl)
- [Two-button lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/advanced/stl/workshop-lid-buttons-2.stl)
- [Two-button insert](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/advanced/stl/workshop-lid-buttons-2-insert.stl)
- [LCD lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/advanced/stl/workshop-lid-lcd.stl)
- [Dual encoder lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/advanced/stl/workshop-dual-encoder-lid.stl)
- [Honeycomb/Saitek adapter](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/honeycomb-adapter-short.stl) (optional)

## Assembling the boards

To assemble the prototyping board and Mega 2560 Pro Mini, connect the Mega to the back of the prototyping board. Then, connect one end of the USB cable to the Mega and the other end of the cable to your computer.

## Installing the firmware and board configuration

{{% steps %}}

### Install MobiFlight

Use the [getting started guide](/getting-started/) to install MobiFlight.

### Upload the firmware

Follow the [flashing ambiguous boards guide](/guides/flashing-ambiguous/boards/) to upload the correct firmware to the Mega 2560 Pro Mini.

### Upload the board configuration

Use the [installing configuration guide](/guides/workshops/installing-configuration/) to upload the standard configuration for a prototype board to the Mega.

{{% /steps %}}

## Assembling the micro-switches

{{< screenshot image="micro-switch-assembly.png" title="Photo of the advanced project with the two micro-switches highlighted." >}}

Insert the micro-switches into the lid and attach the PCB from behind with M3 screws. Plug in the XH-JST 3-pin cable, and pass it through the back of the case.

The micro-switches are connected using XH-JST 3-pin cables. Connect the top switch to `SWITCH 1 (ON-ON)` on the breakout board.

{{< screenshot image="micro-switch-connection.png" title="Photo of a prototype board with the connection for the micro-switches highlighted." >}}

## Assembling and connecting the LCD

{{< screenshot image="lcd-assembly.png" title="Photo of the advanced project with the LCD highlighted." >}}

Assemble the LCD into the case lid with M3 screws. Connect the XH-JST 4-pin cable to the back of the LCD, making sure to connect the black wire to **GND**, then pass the wire through the back of the case.

The LCD is connected using a XH-JST 4-pin cable. Connect the display to `LCD 1` on the breakout board.

{{< screenshot image="lcd-connection.png" title="Photo of a prototype board with the LCD connection highlighted." >}}

## Assembling and connecting the dual encoder

{{< screenshot image="dual-encoder-assembly.png" title="Photo of the advanced project with the dual encoder highlighted." >}}

Assemble the encoder into the case using M3 screws to attach the PCB to the back of the lid. Pass the cable through the hole in the back of the case, then close the lid. Bending the cable 90 degrees, close to the PCB, helps make everything fit.

The encoder is connected using two XH-JST 4-pin cables. Connect the encoder PCB `INNER SHAFT` connector to `ENCODER 1`, and the `OUTER SHAFT` connector to `ENCODER 2`, on the breakout board.

{{< screenshot image="dual-encoder-connections.png" title="Photo of a prototype board with the dual encoder connections highlighted." >}}

## Configuring MobiFlight

The inputs and outputs are configured in MobiFlight by following the guides for each device type:

| Device description        | Device name      | Guide                                                             | Preset category             | Preset name                                 |
| ------------------------- | ---------------- | ----------------------------------------------------------------- | --------------------------- | ------------------------------------------- |
| Dual encoder - outer knob | `ENCODER 1`      | [Configuring encoders](/devices/encoder/configuring-input/)       | Microsoft / Generic / Radio | COM_RADIO_WHOLE_DEC and COM_RADIO_WHOLE_INC |
| Dual encoder - inner knob | `ENCODER 2`      | [Configuring encoders](/devices/encoder/configuring-input/)       | Microsoft / Generic / Radio | COM_RADIO_FRACT_DEC and COM_RADIO_FRACT_INC |
| Dual encoder - button     | `ENCODER 2 PUSH` | [Configuring buttons](/devices/button-switch/configuring-button/) | Microsoft / Generic / Radio | COM_STBY_RADIO_SWAP                         |
| LCD                       | `LCD 1`          | [Showing multiple pages on an LCD](/guides/multiple-page-lcd/)    | See guide                   | See guide                                   |
| Micro-switch - up         | `Switch 1-1`     | [Showing multiple pages on an LCD](/guides/multiple-page-lcd/)    | See guide                   | See guide                                   |
| Micro-switch - down       | `Switch 1-3`     | [Showing multiple pages on an LCD](/guides/multiple-page-lcd/)    | See guide                   | See guide                                   |

## Next steps

With the project assembled, run Microsoft Flight Simulator, spawn in an aircraft like the Cessna 172, ensure the **Run** button is active in the MobiFlight toolbar, and try everything out.

Learn more about using MobiFlight in the [getting started guide](/getting-started/), discover additional supported [devices](/devices/), and join the [MobiFlight Discord](https://github.com/mobiflight) to share your project with other enthusiasts.
