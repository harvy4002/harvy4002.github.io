---
layout: post
title: o2 Joggler - Stock OS
date: 2010-05-06 16:59
author: admin
comments: true
categories: [Computing]
---
Just got my hands on a brand new o2 Joggler for only £50. Now there is a quite a bit of debate as to whether it is worth that much but I think it is. Why you may ask? Well let's look at the specs.

So it has a 1.3Ghz Intel Atom Z520, 512Mb RAM and 1Gb internal flash storage. Very decent spec, almost on par with netbooks. All for £50 when netbooks are on the £200 mark? Well the main drawback is that it is mains powered only. I hope someone comes out with a battery hack. The low storage space is a bit of a problem but that can be overcome with a giant USB stick :-D

So what can be done with it? So after some research there are some interesting possibilities.

<span style="text-decoration: underline;">Stock OS</span>

The stock OS is based on a Ubuntu. But the device is pretty much locked down from the off. So there will be an immediate need to hack to get telnet working.

The o2 Joggler device is actually produced by OpenPeak. They basically rebranded their own product the <a href="http://www.openpeak.com/OpenFrame.php">OpenFrame</a> for o2. Their product seems to have a lot more applications then o2's offering. So if they are both running the same OS but with different applications can we get OpenFrame apps to work on the o2 device (much like running my fav chrome extensions on Iron)? Well it seems you can.

First, you will have to enable telnet on the device. Instructions are <a href="http://jogglerwiki.info/index.php?title=Installing_Telnet">here</a>, its also worth doing it permanently as it's good to have a back door just in case ;-)

Once that is done, time for terminal hacking. I did this via putty. Just Telnet to the device with its IP address and then enter the username: letmein

Now the OS is very basic. All it does is run flash programs so there are two way it can be manipulated to play any kind of flash file.
<ol>
	<li>Log in via terminal and run any hosted or networked swf file from the command line.</li>
	<li>Place an icon on the home screen and hardcode the link in the application config file</li>
</ol>
<span style="text-decoration: underline;">Creating the icons</span>

Here is a very good video on how to install the openframe applications

<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="400" height="300" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,40,0"><param name="src" value="http://www.youtube.com/watch?v=BMgFnog3Qcw" /><embed type="application/x-shockwave-flash" width="400" height="300" src="http://www.youtube.com/watch?v=BMgFnog3Qcw"></embed></object>

Now using this you can only install the pre-made applications for the device. This is done by simply downloading the appropriate file and placing it in the correct folder. A list of the files and folders (to be created) are <a href="http://jogglerwiki.info/index.php?title=OpenPeak_Apps_list">here</a>.

Next up is allowing custom flash files to run on the device. Simply by setting the location of the application case...

<span style="text-decoration: underline;">Via Teminal</span>

This allows you to run flash file straight form the command line, basically remote controlling the device.

This allows the possibility of controlling the device remotely and running any flash file on command. Basically you telnet in and access the /openpeak/tango directory. Then run ./localrun with the url of the flashfile you want to run.
