---
layout: post
title:  "SMD Board Assembly"
date:   2016-9-29 8:47:58 -0800
categories: jekyll update
---
Well, we ordered 23 sets of components and 20 PCBs of the new circular rev, and they've come. We ended up getting 25 PCBs, which is pretty nice--our PCB manufacturer Elecrow just added them on presumably because they fit in the original panel they cut the PCBS out of.

[pcbs photo]

We tried to have a build session where we'd set up an assembly line to make the sensor boards. Instead of the parts moving to us, however, we'd move around a central table that had the parts.

We'd tape the boards down with a bit of space in between each one. The first person would come around applying solder to each board, by dragging a blob of solderpaste over the PCB stencil, which in turn is lined up exactly with the pads of the PCB. 

[photo of everything lined up]

The next couple folks would come by placing components. We'd try to place complicated, expensive components first (like the processor, which has a bunch of pins very close together) and then place cheaper passive components, which are less complicated.

[atmega328 vs a capacitor comparison]

The boards would then be reflowed in the oven, melting the solder paste and causing the components to be conductively adhered to the board. 

However, this didn't work as well as planned. For one, we forgot to buy one of the components, a bunch of 10uF capacitors. So we were only able to make around 12.

For those we did get to, we applied way too much solderpaste to the board, which caused short circuits after reflowing. Because there was too much conductive material on each pad, many of them combined after reflowing. The effect was that some components had two pins that were conductively joined, which would certainly cause us problems if we gave them power. 

[too much solderpaste close ups]
