---
layout: post
title: Hacking the Powershot
date: 2010-07-18 17:16
author: admin
comments: true
categories: [Technology]
---
Well my Canon Powershot A470 arrived today, after the eBay seller just took way too long to deliver it. Over a week and a half!!!

[caption id="attachment_311" align="alignleft" width="300" caption="Just unboxed Canon A470"]<a href="http://blog.havinderatwal.com/wp-content/uploads/2010/07/DSC04249.jpg"><img class="size-medium wp-image-311" title="Canon" src="http://blog.havinderatwal.com/wp-content/uploads/2010/07/DSC04249-300x225.jpg" alt="" width="300" height="225" /></a>[/caption]
<p style="text-align: left;">So I actually completely forgot about it till the postman rang, then I was tingling with anticipation as I was opening the box. But why you ask? On the surface it is just a bog standard camera.</p>
<p style="text-align: left;"></p>
<p style="text-align: left;"></p>
<p style="text-align: left;"></p>
<p style="text-align: left;"></p>
<p style="text-align: left;"></p>

<blockquote style="text-align: left;">7.1 MP

3.4X Optical Zoom

Face Detection
<p style="text-align: left;">Up to ISO 1600</p>
1cm Macro (That's pretty good)

Movie mode

Supports SDHC (A must nowadays)</blockquote>
<p style="text-align: left;">For a camera that old (Jan 2008) it has some pretty cool tech inside but that was not why I spent £40. The fact is, it is a Powershot and it can be hacked with CHDK. CHDK(Canon Hack Development Kit) is some software that you install on the SD card and the run hacked software from the card to add some cool new features to the Canon OS (runs like a Live OS CD). <a href="http://lifehacker.com/387380/turn-your-point+and+shoot-into-a-super+camera">Here's a nice article</a> from LH to outline the basic features of CHDK.</p>
<p style="text-align: left;">So now to see how easy is it to load up the new software and what extra things can I do with it. I am already excited.</p>
<p style="text-align: left;"><span style="text-decoration: underline;">Boot up</span></p>
<p style="text-align: left;"></p>


[caption id="attachment_312" align="alignright" width="300" caption="Super Macro for the Canon A470"]<a href="http://blog.havinderatwal.com/wp-content/uploads/2010/07/IMG_3134.jpg"><img class="size-medium wp-image-312" title="supermacro" src="http://blog.havinderatwal.com/wp-content/uploads/2010/07/IMG_3134-300x225.jpg" alt="" width="300" height="225" /></a>[/caption]
<p style="text-align: left;">After a bit of battery trouble I have managed to get the camera to boot natively. Tried out a few features the 'super marco' is really good, this is probably the first camera I have owned that has that feature. I did own a slim line Sony T9, which sucked at low light and macro. But aside from that the features are very basic, just what you would expect from a point and shoot. It has 3 modes of photo taking Automatic, Manual and Scene(cut down version of manual with profiles for different scenes, portrait, snowy, etc). It also has a video option but I guess I am not interested in that for now.</p>
<p style="text-align: left;">So we load up CHDK for the camera, first up is to find the firmware version of that camera, now my model has 4 different versions. So I used <a href="http://chdk.wikia.com/wiki/FAQ#Q._How_can_I_get_the_original_firmware_version_number_of_my_camera.3F">this</a> to find out what it is. Once that is done then just download the appropriate files to place on your SD card then update the firmware from the camera with the card inside. As far as I know it just keeps the newly loaded files in memory, so all is good if everything starts to go haywire.There are very good guides on how to access the new menus and how to use CHDK. Here are a few links to get you started:</p>
<p style="text-align: left;"><a href="http://chdk.wikia.com/wiki/FAQ">http://chdk.wikia.com/wiki/FAQ</a></p>
<p style="text-align: left;"><a href="http://chdk.wikia.com/wiki/CHDK_User_Manual">http://chdk.wikia.com/wiki/CHDK_User_Manual</a></p>
<p style="text-align: left;"><a href="http://chdk.wikia.com/wiki/Cardtricks">http://chdk.wikia.com/wiki/Cardtricks</a> - useful automated tool for getting CHDK on your card and making it bootable</p>
<p style="text-align: left;">The basic idea is that scripts are made by developers to things that you couldn't normally do with the camera. These scripts are written in BASIC (one of the first languages I learned), so it opens the possibility for me to write my own scripts :-) But that is a whole other project.</p>
<p style="text-align: left;">So here are some of my favourite features:</p>

<ul style="text-align: left;">
	<li>Reversi - Yes you can play games on your camera, always the acid test when trying to hack anything with a screen and buttons</li>
	<li>HDR shooting - Basically changes the exposure setting in a range of shots to be combined for a HDR photo</li>
	<li>Intervalometer - Can take unlimited time lapse photos</li>
	<li>RAW format - Yes, you can.</li>
</ul>
<p style="text-align: left;">Now wouldn't it be great if it CHDK loaded with your camera instead of faffing about with the whole upgrade firmware option just to get it running every time you start up the camera? Well you can but it requires a bit of work. So first the SD card has to be formatted in to FAT-16 which is what the camera needs to boot up, for some reason :-S Now the examples it gives for the next step on the CHDK website just seems to flag the card as a removable hard drive then bootable (it's basically one bit flag that gets flipped) now since I have my own tools for that I ignored what they did and just followed my own route. If it is too confusing for you then just use the link above for the CardTricks program.</p>
<p style="text-align: left;">I'm sure in the future I will putting up a post of my own scripts for the camera but until then this was a good hack.</p>
