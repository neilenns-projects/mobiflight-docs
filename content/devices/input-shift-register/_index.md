---
title: Input shift registers
description: How to use input shift registers with MobiFlight
---

As you continue to build panels you may encounter situations where you have more buttons for input than there are pins available on your Arduino. The solution is to use an input shift register like the [74HC165](https://www.ti.com/product/SN74HC165). These allow you to read input from eight buttons while only using three pins on the Arduino.

MobiFlight supports up to 32 bits of shift registers in a chain (typically four eight-bit chips), and up to six chains of input shifters can be connected to a single Arduino.

## Popular options

The chip is available anywhere you buy electronics, including [Amazon](https://www.amazon.com/Bridgold-SN74HC165-74HC165-Parallel-Load-Registers/dp/B095KNTCKN/ref=sr_1_3?crid=293SFF21893S9&keywords=74hc165&qid=1641735408&sprefix=74hc16%2Caps%2C383&sr=8-3), [eBay](https://www.ebay.com/sch/i.html?_from=R40&_trksid=p2380057.m570.l1313&_nkw=74hc165&_sacat=0), [AliExpress](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20220109053846&SearchText=74hc165+dip), [Tayda Electronics](https://www.taydaelectronics.com/74hc165-74165-ic-8-bit-shift-register.html) and [many other parts suppliers](https://octopart.com/search?q=74HC165&currency=USD&specs=0&case_package=DIP&case_package=PDIP).
