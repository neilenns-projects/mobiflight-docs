---
title: Getting started
breadcrumbs: false
description: How to start using MobiFlight with flight simulators
weight: 10
---

MobiFlight is a powerful tool to control your flight simulator with a [board](/boards/) and [wide range of devices](/devices/). The choices can be overwhelming at first, so we recommend getting started with a simple parking brake switch and indicator LED.

The following video provides complete instructions for those two projects:

{{< youtube id="pS8KGfYRNrY" title="Getting started with MobiFlight" >}}

Here are the basic steps:

{{% steps %}}

### Close your flight simulator

If you use Microsoft Flight Simulator 2020 or Microsoft Flight Simulator 2024, close it before installing
MobiFlight.

### Download and install MobiFlight

Download the latest release from the [MobiFlight website](https://www.mobiflight.com/en/download.html) and
run the installer. MobiFlight will launch automatically after install completes.

### Connect a board to your PC

Connect a [supported board](/boards/) to your PC and when prompted by MobiFlight install the matching
firmware.

> [!TIP]
> Some boards cannot have their type automatically determined by MobiFlight. If that happens, see the
> [flashing ambiguous boards](/guides/flashing-ambiguous-boards/) guide.

### Add an LED device and output configuration for the parking brake indicator

See the [LED tutorial](/devices/led/) for complete steps on how to wire the LED and create the output configuration.

### Add a switch and create an input configuration for the parking brake

See the [buttons and switches tutorial](/devices/button-switch/) for complete steps on how to wire the switch and create the input configuration.

### Start the sim and try it out

With everything configured, launch your flight simulator, spawn in a plane at a gate, and make
sure to hit the run button in the top bar of MobiFlight's main window to start MobiFlight's connection
to the simulator.

Then toggle your parking brake switch and watch the parking brake change state and the LED light up
to show the state!

{{% /steps %}}
