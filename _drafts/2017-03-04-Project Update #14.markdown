---
layout: post
title:  "Sent to Costa Rica!"
date:   2017-03-04 11:08:00 -0800
categories: jekyll update
---
We have reached a major milestone in our project: sending down prototype sensors to the Leatherback sensors in Costa Rica! We've been working hard over the last couple months to get them ready, so here's an update of what we've accomplished.

* We finished release 0.1.0 of our data downloading software, which looks for an Arduino connection, reads the data off the sensor, and synchronizes said data to real time. As we mentioned (briefly)[link] earlier, our sensor reads absolute time, or time since last reset (i.e. when the sensor is turned on). To match this with the time in the real world, we synchronize time in two ways. The added complexity in this is that our clock and sensor are not 100% reliable. The crystal oscillator that tracks time for us might have a tolerance of +/- 5%, which means that if it records a reading every 30 minutes that reading could actually take place anywhere between 28.5 and 31.5 minutes. Plus, it's possible the sensor could reset either because of an overflow (when the time gets so large it becomes too long for the data type to handle) or because of any other freak event.
	* The sensor firsts synchronizes the time assuming that the last reading corresponds to the current local time--basically working backward through the data based on the final reading.

	* We then ask the user to input what he/she recorded as the starting time of the sensor, or when they put on the battery and screwed down the case. Depending on how accurate this is to our basic synchronization, we do 1 of 2 things. 

	* If it's pretty accurate, we assume that error derives from the crystal oscillator and so stretch or shrink the data to have an even repeated interval. Below is a graph of the data before and after synchronization.

	* If, in contrast, the starting time the researcher entered is way different from our calculated start time, we can only assume the sensor turned on and off or something else funky happened. We correct for this by assuming that each interval was an exact 8 seconds --while this is not a perfect solution, the raw data is also included so that researchers can flag if there's a big gap in the data or something. 
	
	The code for the data downloader is publicly available on GitHub (here)[https://github.com/leatherback-monitoring/DataParser]. From a user experience perspective, the program is very basic: it is entirely run in the command line, asking the user questions and validating answers to compute its result. However, it was still an interesting exercise in understand the user experience in the data downloading software: which questions were asked when, how they were worded, and what feedback the program outputted to the user all had to be considered. The backend of the datadownloader was no small feat either--we had to make sure that the software would find an incoming serial detection and send the sensor a "Read" command to download 

* We created a nice 
