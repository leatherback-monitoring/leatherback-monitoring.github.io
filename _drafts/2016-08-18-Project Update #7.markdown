---
layout: post
title:  "Tangents"
date:   2016-08-18 10:28:39 -0800
categories: jekyll update
---
This project has been at least partly a journey of dead ends, rabbit holes, and tangents. 

One of those tangents was realizing that because our sensor was going into the prenatal (is it prenatal if it's an egg?) habitats of endangered animals, they probably shouldn't have lead or other nasty chemicals that could harm said endangered animals. Oops. We ended up poring over MSDS documents and datasheets to make sure our components were a) RoHS (Removal of Hazardous Substances) compliant and b) lead-free. We also checked to make sure the case material we used (PLA) didn't degrade into tiny little bits of plastic over time--and we're currently running a test to see if that's true. 

My technical definition of a "rabbit hole" is a long path that you go down only to realize you didn't need to go down it. Our rabbit hole was the realization that a square case is probably not as good as a circular one. Why? A square case has sharper corners, which has the potential to damage sea turtle eggs. It uses screws and nuts, which can be replaced with a circular 3D printed thread, saving us money and assembly time. It also requires us laser-cutting a silicone gasket, which again takes time and money. Instead, we can use just an off-the-shelf o-ring to make sure we get a good seal. Yes, there's the downside that a circular PCB is less space efficient than a square one, but because our board is still pretty small, it doesn't cost any more money to make. 

The main downside, however, is that all of the design work to make the best square turtle sensor ever is "wasted." I put wasted in quotes because it's really not--the prototype taught us something about our design. Only after investing the time into developing a square prototype could we see that circular sensors were better.

That means the PCB layout Erik worked down to 30x30mm had to be re-arranged for a circular shape. It means the time Matthew spent working on selecting the best material and shape for the gasket, plus the CAD refinement of a square case, is no longer relevant. So it goes.

And a dead end? At the beginning of the project, we investigated buying an off-the shelf case that we could be sure was waterproof. We ended up going custom because of the flexibility it provided us, but Matthew got all sorts of quotes from Alibaba and learned about the complicated nature of buying wholesale in China.

I've seen diagrams that show how non-linear the design process can be, and I think this project is a great example of it. 

![The Design Process](/assets/designprocess.jpg "The Design Process")