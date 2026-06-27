---
title: "LCR Detective"
author: "Varun"
description: "A DIY LCR Meter with multiple channels employing different measurement stratergies/architectures"
created_at: "2026-06-27"
---

# June 27: Exploring Impedance measurement stratergies (Auto balancing Bridge)

I've checked/explored the functioning of the auto-balancing bridge method, and it really seems that the frequency at which I
can/will be able to trust the impedance measurements is going to be really low, unless I splurge on a really high-end OPA.
So far it seems that the generic OPA from Gansil (GS4580-DR) will get me close to around 100kHz, with me feeling that the range
will increase the lesser amount of the current I pass through the DUT (the virtual ground seems to be properly maintained when
the current requirement is low, this might be worth investigating later).

On further analysis, since I'll need to pass lower currents, having an appropriately large resistor to introduce a large gain
is inevitable, and with it the introduction of high amounts of noise. Seems like this is basically a dead-end for this architecture.

After looking at the schematic of existing LCR measurement jigs from Texas Instruments, I've found out that the GBP (Gain bandwidth
Product is a really important factor, If I want to achieve proper impedance measurements at higher frequencies).

And now finally, I've also encountered some stability issues with the feedback loop, leading to some resonance/ringing.I'll end this
session here, and I'm hoping to make more progress in the next session.


**Total time spent: 1 Hour 1 Minute**
