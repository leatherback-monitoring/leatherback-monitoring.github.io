---
layout: post
title:  "Project Update #5:Prototyping Continues"
date:   2016-04-30 4:31:28 -0800
categories: jekyll update
---
The through-hole prototype is all but finished--we're just having an issue getting the flash memory to work. Since we've tried all three of the flash chips we've ordered, we're wondering if maybe one from another manufacturer will do better--so we've made a little breakout board to go on our prototype.

Due to a software update with the OtherMill combined with the use of a new tool, our PCB machining speed has greatly improved! We can now cut the board in only a few minutes time. Here's a video of the machine cutting out the profile for one of our PCBs.

<iframe width="420" height="315" src="http://www.youtube.com/embed/6P0oIzekGDM" frameborder="0" allowfullscreen></iframe>

In other electronics hardware news, Erik got a reflow oven for his birthday! The reflow oven is basically a glorified toaster oven that heats up at a predefined profile. For example, it might heat quickly for 10 minutes, stay at a certain temperature for 5, increase slowly then decrease slowly, maintain a different temperature, and then cool slowly. 

![The Reflow Oven](/assets/thereflowoven.jpg "The Reflow Oven")

The model Erik received is the T962, which is a low-cost entry-level model that has so many technical flaws it's documented in a [GitHub repository](https://github.com/UnifiedEngineering/T-962-improvements). We spent a few hours making these upgrades--adding a better temperature monitor, flashing the firmware, replacing the masking tape that made it smell funny, etc. 

The device allows us to make Surface Mount Device (SMD) circuit boards, whcih just means that you're using components that are tiny versions of the electronics components that most hobbyists use. SMD components are used in manufacturing when the size of the board is a high priority, which it usually is. We initially didn't use SMD components so that we could assemble the boards more easily--SMD components get so small they are hard to move around accurately--but once we had the design fleshed out enough we moved into SMD land and reduced the size of our board from 72mm square to 30mm square. Here's a photo just to see how much of a difference it makes using SMD components!
![The Two Prototypes](/assets/thetwoprototypes.jpg "The Two Prototypes")

In terms of the case design, we have selected three different options for a breather vent and are doing some testing to determine which one is most water resistant while still letting in water vapor. We have the task of trying to make a sensor that is both waterproof and can measure humidity...which is impossible. In order to read humidity, you need to have some way of letting air (moist air) into the sensor, which makes the sensor waterproof. So in the end, we're shooting for water resistance.
![The Three Ports](/assets/thethreeports.jpg "The Three Ports")


