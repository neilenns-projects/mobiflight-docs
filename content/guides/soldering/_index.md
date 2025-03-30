---
title: Making good solder connections
description: Tips and tricks to making good solder connections when working with devices.
---

Good soldering connections are key to a successful custom cockpit build. Poor quality solder joints result in intermittent issues, particularly when working with [7-segment displays](/devices/seven-segment-display/).

High-quality connections look like this:

{{< screenshot image="good-soldering.png" title="Photo of a board with four good quality solder connections." >}}

## Soldering tips

{{% steps %}}

### Follow a YouTube tutorial

YouTube has several tutorials that provide a short but thorough introduction to proper soldering technique. The following video is a good reference for soldering through-hole components.

{{< youtube id="vAx89WhpZ3k" title="Soldering through-hole components" >}}

### Use the correct soldering iron temperature

A soldering iron set to too low a temperature makes it difficult to melt the solder and results in pins that are poorly connected to the board pads. These temperatures are a good starting point:

| Solder type | Celsius   | Fahrenheit |
| ----------- | --------- | ---------- |
| Lead-based  | 315--370° | 600--700°  |
| Lead-free   | 350--400° | 660--750°  |

The higher end of the temperature range may be necessary when soldering ground pins.

### Use high-quality solder

Solder from sites like AliExpress, while inexpensive, are generally low-quality and are frustrating to use when soldering. Always buy a reputable brand with high ratings and good reviews.

### Add flux

Most solder includes a core of flux, which is sufficient when making new solder connections. When reworking existing connections, adding additional flux with a [rosin flux pen](https://www.amazon.com/MG-Chemicals-Rosin-Flux-Pen/dp/B0080X79HG) to the existing joint can dramatically improve the quality of the soldering. Applying flux is also helpful when removing excess solder from a joint.

{{< screenshot image="rosin-flux-pen.png" title="Photo of a rosin flux pen." >}}

### Clean the soldering iron tip

Keeping a soldering iron tip clean is crucial for achieving strong, reliable solder joints. A clean tip ensures efficient heat transfer, allowing the solder to flow smoothly and bond properly with the components.

Regularly wiping the tip on a damp sponge or [brass wool](https://www.amazon.com/Hakko-599B-02-Wire-type-soldering-cleaner/dp/B00FZPGDLA) and re-tinning it with fresh solder helps maintain a clean, well-functioning tip, ensuring consistent results.

### Apply heat to the joints

Make sure the soldering iron is applying heat directly to the component lead and the board pad before applying the solder. Heating the solder directly with the iron, and not heating the leads or board pad, results in a poor quality connection.

{{% /steps %}}

The two most common issues with soldered connections are **cold or incomplete connections** and **shorted connections**.

## Cold or incomplete joints

Cold or incomplete connections occur when the soldering iron temperature was set too low, the soldering iron tip was dirty, or enough solder wasn't applied. These joints look like this:

{{< screenshot image="cold-joint.png" title="Photo of a board with four incorrectly soldered joints that lack enough solder to make a reliable connection." >}}

To resolve the issue, apply a bit of flux to the existing connections and reheat the joints, applying more solder as necessary.

## Shorted connections

Shorted connections result when too much solder was applied, resulting in a bridge between two adjacent pins. These connections are sometimes subtle, resulting from a small solder connection between the pins. Excess solder on a pin can also cause intermittent bridging when the board is flexed or moved.

{{< screenshot image="solder-bridge.png" title="Photo of a board with four incorrectly soldered joints. Two are bridged with solder, and two have an excess amount of solder." >}}

To resolve the issue, apply a bit of flux to the shorted connections and reheat the joints with a clean soldering iron tip. Pull the iron away from the joint, taking some of the excess solder, and repeat as necessary until the short is removed. Make sure to clean the soldering iron tip every time before reheating the shorted connection.
