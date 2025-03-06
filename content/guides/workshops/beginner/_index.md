---
title: Beginner workshop
description: Ste-by-step guide to configuring the beginner workshop project with MobiFlight.
weight: 20
---

The beginner workshop builds a panel that includes toggle switches, illuminated push buttons, and an encoder to control a parking brake and autopilot heading, and to display the current state of the parking brake.

## Required components

The following components are required for the project:

| Part                                                                                       | Quantity |
| ------------------------------------------------------------------------------------------ | -------- |
| [Mega 2560 Pro Mini](https://shop.mobiflight.com/product/arduino-mega-2560-pro-mini-usb-c) | 1        |
| [MobiFlight prototyping board](https://shop.mobiflight.com/product/prototyping-board-v2)   | 1        |
| [Enclosure](#3d-printed-enclosure-parts)                                                   | 1        |
| [LED push button](/devices/button-switch/)                                                 | 2        |
| [Encoder with breakout board](https://shop.mobiflight.com/product/single-encoder-bundle)   | 1        |
| [ON-ON switch](https://shop.mobiflight.com/product/switch-12mm-panel-mount)                | 2        |
| MobiFlight switch breakout board                                                           | 1        |
| XH-JST 2-pin wire                                                                          | 2        |
| XH-JST 3-pin wire                                                                          | 3        |
| XH-JST 4-pin wire                                                                          | 1        |
| M3x5mm screw                                                                               | 12       |

## 3D printed enclosure parts

The following parts make up the 3D printed enclosure:

- [Base](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/workshop-beginner-base.stl)
- [Dual push button lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/workshop-dual-pushbutton.stl)
- [Dual toggle switch lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/workshop-dual-toggle-switch.stl)
- [Encoder lid](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/workshop-encoder.stl)
- [Honeycomb/Saitek adapter](https://github.com/MobiFlight/MobiFlight-Connector/wiki/images/workshops/beginner/stl/honeycomb-adapter-short.stl) (optional)

## The prototyping board

The beginner workshop uses a [MobiFlight prototyping board](https://shop.mobiflight.com/product/prototyping-board-v2) to connect devices to the [Mega 2560 Pro Mini](/boards/recommended/mega-2560-pro-mini) board.

{{< screenshot image="beginner-connections.png" title="Photo of the MobiFlight prototype board v2 with the beginner workshop connections highlighted." >}}

Devices connect to the prototype board as follows:

| Device                 | Connector          |
| ---------------------- | ------------------ |
| LED - Push button 1    | `LED 1 PWM`        |
| Button - Push button 1 | `Button 1`         |
| LED - Push button 2    | `LED 2 PWM`        |
| Button - Push button 2 | `Button 2`         |
| Switch - Toggle 1      | `Switch 1 (ON-ON)` |
| Switch - Toggle 2      | `Switch 2 (ON-ON)` |
| Encoder                | `Encoder 1`        |

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
