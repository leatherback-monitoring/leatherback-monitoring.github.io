---
layout: post
title:  "Breadboard Prototypes"
date:   2016-03-06 15:21:36 -0800
categories: jekyll update
---

Typically, the first step in designing an electronics project is prototyping. And the most common first prototype is a breadboard.

![A Breadboard](/assets/breadboard.jpeg "A Breadboard")
<span style="font-size: .5em"> Sparkfun </span>

A breadboard is a nifty little device that is an array of electrically connected 4-pin rows. There are two sets of these 4 pin rows, which run along the center of the the board. On each side, there are conductive two rows running the length of the bread, each set of 2 can be used as a power and ground.

![Back of Breadboard](/assets/breadboardback.jpeg "A Breadboard")
<span style="font-size: .5em"> Sparkfun </span>

The nice thing about breadboards is that they allow you to easily and temporarily connect different bits of electronics together. In our case, we've started by creating a prototype composed of an Arduino, breakout boards, and other passive components (often referred to as passives). 

![Our Breadboard Prototype](/assets/ourbreadboardprototype.jpg "Our Breadboard Prototype")

I'll break each one of these down below.

1) Arduino

The Arduino is an awesome microcontroller developed in Italy. It uses an ATMEGA328 processor and is a great introduction to microcontrollers and electronics. We're using it primarily because its programming language (Arduino, based off of Processing) is well supported, and also because there's a lot of companies and makers that create tools that can interface with Arduino. We also have prior experience working with Arduino, which will come into handy when we're debugging strange errors that are sure to pop up.

Arduinos come in all shapes and sizes, with a range of features: 

![Arduino Variants](/assets/arduinovariants.jpg "Arduino Variants")

For our breadboard prototype, we'll be using an Arduino Pro Micro, which is very similar to the Pro Mini but is made by Sparkfun. One of the best parts of Arduino is that it's open source, which means that other companies can make Arduino "clones" and sell them with other features or decreased price. 

2) Breakout Boards

A breakout board takes an electronic component and makes it easy to interface with other electronics components, especially Arduinos and other microcontrollers. For example, let's say you want to connect your Arduino to a USB female port.

This is what a bare bones female USB port looks like: no cable, no covering, no nothing:
![Female USB Port](/assets/usb.jpg "Female USB Port")
The USB port has some very closely positioned pins that would be hard to connect to Arduino's general input and output (GPIO) pins. 

To solve this issue, we'd use a female USB breakout board: 
![Female USB Breakout Board](/assets/usbbreakoutboard.jpg "Female USB Breakout Board")

The breakout board provides a series of holes to which you can solder the same kind of header pins the Arduino uses. You can then connect the breakout board to the Arduino with jumper wires.

3) Passives
Passive components are pretty simple. The official definition for passive components is that they cannot control current through an external electrical signal. Passives include resistors, capacitors, motion sensors, and thermocouples. Active components include didoes, transistors, integrated circuits (ICs), and display components.

Now, this was a lot of tutorial. Now onto our actual device. We reposted the image for your mental refreshment. 

![Our Breadboard Prototype](/assets/ourbreadboardprototype.jpg "Our Breadboard Prototype")

The breadboard prototype connects the individual components that make up an Arduino to an SMD 