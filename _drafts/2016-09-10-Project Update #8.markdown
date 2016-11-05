---
layout: post
title:  "The Case Evolution"
date:   2016-9-10 6:45:24 -0800
categories: jekyll update
---
Both the electronics and its protective case have undergone a number of significant revisions and iterations; for this post, I'll be focusing on the case. The case presents the unique challenge in that it's required to be as waterproof as possible while still allowing measurement of humidity, which takes place on a sensor module inside the case. Those are two mutually exclusive things--humidity measurement requires some kind of opening that water vapor can pass through, waterproofing in its most simple form is blocking all openings. 

We've tired a bunch of different solutions to strike a balance. First, we tried using a couple of breather vents from McMaster Carr--one with louvered panels, another that advertised itself as "liquid-tight."

![Port Comparison](/assets/portcomparison.jpg "Port Comparison")

We realized that some options were too porous, and some weren't porous enough. We eventually settled on using sintered metal filters as a humidity port, which are densely packed disks of sintered steel that resist the ingress of liquid water but allow for passage of gases through the screen. 

![Sintered Metal Filters](/assets/sinteredmetaldisks.jpg "Sintered Metal Disks")

What's confusing sometimes about these kinds of products is they don't specific what part of the product is waterproof/water resistant/some other kind of ingress protection.

For example, a switch we bought calls itself IP67--which just stands for Ingress Protection level 67. The first digit, 6, refers to dust resistance (greater is better), the second is for water resistance. There are specific tests you can do to determine the IP rating of your product. But it wasn't clear to us whether the IP67 rating was for the entire switch, or the switch if you mounted it according the manufacturer's constructions. What happens if the leads get wet? Deep questions that still remained to be answered....

Another aspect of weatherproofing we've been looking into and testing out is conformal coating. Conformal coating is a process in which a thin layer of protective chemical (usually some kind of acrylic, polyurethane, epoxy, or siliocne) is deposited on a PCB through dipping, spraying, painting or curing. There are advantages to each type of material and coating method, but we're looking into spray acrylic as it's easy to apply and relatively easy to rework (remove & redo if something goes wrong or needs to be tested). However, we can't conformally coating the opening of our humidity sensor, because then it would be unable to log humidity.

The last part of weatherproofing the sensor is the union between the two distinct parts of the case. As the case is now a roughly circular shape, two pieces will screw together. It's tricky to get the tolerancing right of the screw threads because the 3D printer we're using doesn't have great repeatibility. However, we're confident a combination of 3D printer maintenance tweaks and CAD tolerancing in good threading action. 

The first version was just a prototype, much smaller than it was eventually going to be. Regardless, it fit together without engaging the screw threads--just too small.

!["First Iteration Threading"](/assets/firstthreading.gif "First Iteration Threading")

The next iteration was full size, but didn't screw together. I think the tolerances and design were off on this one--it was too tight--but a few more hours of tweaking yielded this:

!["Too Tight threading"](/assets/threadingtootight.gif "Too Tight Threading")

With a bit of lubricant (olive oil), our third iteration screwed together, but the initial action was clunky--it took a few tries to get the first bit of thread to engage. We tweaked the design some more and increased our tolerances. We also did some maintenance/tuning to the 3D printer--we were printing at too high of a temperature, causing unecessary strands that were ugly and got trapped in the threads:

!["Nasty 3D Print Strands"](/assets/nastythreads.jpg "Nasty 3D Print Strands")

The next version was too loose, rather than too tight--we had set too large tolerances for the threads.


<img src="http://imgur.com/Wf6P8ol"></img>

The next iteration had tolerancing that was closer to what we wanted, and was nearly watertight. But to further ensure the case stays waterproof, we added an O-Ring to the junction between the two components. The O-Ring is a rubber ring that compresses when the two components are screwed together, forming a seal that should resist water and other chemicals. 

!["Case with O-Ring"](/assets/casewithoring.gif "Case with O-Ring")

To allow for better compression, we angled the outsides of each case part outward to increase the surface area of case that's pressing on the O-Ring.

!["Angled Case Design"](/assets/draftedcase.jpg "Angled Case Design")

Eventually, we ended up with this:

!["Final Threading"](/assets/finalthreading.gif "Final Threading")

We're also striking a balance between filament use and wall thickness in our parts; they're designed to be as thin as possible (to minimzie thickness) while still remaining strong and impermeable to fluids. 

Finally, a heads up: when you export from SolidWorks to an STL, be aware that you can change the resolution of your export (increase or decrease triangle count, etc.). We didn't realize this until later on, but it can actually makes your prints smoother.
