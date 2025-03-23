---
title: Multiplexers
description: How to use multiplexers with MobiFlight.
ogimage: card-images/devices/multiplexer.png
next: /devices/multiplexer/wiring/
---

{{< buy-in-shop url="https://shop.mobiflight.com/product/multiplexer" >}}

When building panels, you may encounter situations where you have more buttons for input than available pins on your board. Multiplexers like the [74HC4051](https://www.ti.com/product/CD74HC4051) (8-bit) and [74HC4067](https://www.ti.com/product/CD74HC4067) (16-bit) allow you to read input from 16 buttons while only using five pins on the board. Additional multiplexers connected to the same board only require one additional pin.

{{< cards >}}

{{< card title="Multiplexer" subtitle="74HC4067 breakout board" image="card-images/devices/multiplexer.png" >}}

{{</ cards >}}

For information on how many multiplexers can be connected to a board, see the [boards](/boards/) documentation.

> [!IMPORTANT]
> MobiFlight only supports connecting buttons to multiplexers. Encoders must be connected directly to a board.

## Popular options

The 16-bit 74HC4067 multiplexer is widely available mounted on breakout boards. The MobiFlight shop sells [individual boards](https://shop.mobiflight.com/product/multiplexer) and a [32-input breakout board](https://shop.mobiflight.com/product/multiplexer-breakout-board).

Other sites selling the 74HC4067 include [Amazon](https://www.amazon.com/s?k=74HC4067), [eBay](https://www.ebay.com/sch/i.html?_nkw=74HC4067), [AliExpress](https://www.aliexpress.us/w/wholesale-74HC4067.html), and [many other parts suppliers](https://octopart.com/search?q=74HC4067&currency=USD&specs=0&case_package=PDIP).

## Additional resources

- [Buy in the MobiFlight shop](https://shop.mobiflight.com/category/boards)
- [74HC4051 datasheet](https://www.ti.com/lit/ds/symlink/cd74hc4051.pdf?ts=1737904695870)
- [74HC4067 datasheet](https://www.ti.com/lit/ds/symlink/cd74hc4067.pdf)
