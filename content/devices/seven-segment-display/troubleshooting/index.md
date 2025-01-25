---
title: Troubleshooting
description: Troubleshooting 7-segment display modules in MobiFlight.
ogimage: card-images/devices/seven-segment-max7219.png
weight: 40
---

7-segment displays, in particular those using MAX7219 drivers, are a common source of frustration. Common issues include digits only partially displaying or the display only showing `88888888` as the value.

To resolve the display problems, check the following items.

## Use an external +5V power supply

MAX7219 displays should not be connected to the +5V pin on a board. The power requirements for the seven segment displays, particularly when wired in series, can easily exceed the power supply limits of the board.

## Run a dedicated +5V power input wire for each display

+5V power should never be daisy-chained when using MAX7219 displays. Always run a dedicated wire from +5V power to the power input pin of each display. The [wiring guide](/devices/seven-segment-display/wiring/) has a schematic that shows this in more detail.

## Use high-quality wires for connections

Dupont wires, while popular, are frequently poor quality and do not provide the solid electrical connections MAX7219 boards require. Elegoo Dupont wires are known to work well. Alternatively, soldering hookup wire between the module and board will ensure a strong connection.

## Verify the pin assignments

It is very easy, particularly on boards with double rows of pins, to connect the display module wires to different pins than expected on the board. Pay close attention to the pins used on the board, then confirm in the [**MobiFlight Modules** dialog](/devices/seven-segment-display/adding-device/) that the pin assignments are correct.

## Try only one module at a time

Daisy-chained MAX7219 introduce additional failure points to the setup. If some boards in the chain are working correctly, and others aren't, try simplifying by only connecting a single module. If that works, add additional modules one at a time, taking care to provide a dedicated +5V power input wire and high-quality connections for each additional module.

## Verify the display modules are good

Cheap MAX7219 modules are common, and it is not unusual for the boards themselves to be bad. Try swapping the display module for another one to see if it resolves the problem. In some cases, modules may work when they receive an input directly from a board, but will fail to pass data signals properly on the output side to daisy-chained boards.
