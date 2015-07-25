---
layout: post
title: My first server
date: 2010-11-20 22:06
author: admin
comments: true
categories: [Computing]
---
Now I say my first server but that isn't strictly true. I have been using my baby Toshy (that's toshiba laptop for the rest of you) for a few years as a general laptop,wireless network bridge and server at different stages of its life.

But now it was time to buy a dedicated sever. Why? Well essentially I wanted a machine that I could mess around without it affecting my normal day-to-day operations. I didn't want to trash my main pc just because I was "experimenting". Also I wanted an "always on" media serving/playing machine. Finally I wanted a dev machine that I could finally get to learn real linux, none of this dual booting nonsense.

So I settled down for a beagleboard-xM. I placed my order and waited..... and waited.... and waited... some more. 4 months later and it still didn't arrive.  Since the beagleboard was made by hobbists it was almost impossible to get hold of one, the back orders in the USA sucked up supply before they could even be shipped over here and even as I write this my order is still waiting.

So I got fed up. I remembered my friend had bought a small server sometime ago, so I asked him for advice and he pretty much recommended what he already had. Now I did some shopping but he seemed to have got the best deal. It was the Acer Aspire Revo 3610.Specs are quite good:
<blockquote>Intel Atom 330 (Dual Core /w HT)

2GB RAM

160GB SATA HD

6 USB ports!!!!! Crazy. and a card reader

HDMI and SPDIF along with your normal audio I/O</blockquote>
This was some serious kit, clocking in at just under £200. (and a free keyboard and mouse)

So I decided this to be my server. It's small form factor made it nice and friendly and the best thing I found out was the power usage. At load it was peaking at 25W!! I'm guessing at load it means pumping full HD and serving out requests. This was my always on requirement fulfilled. Mind you the beagleboard clocked in at 5W, so I am still a bit cautious about the whole "always on" solution. But that is the equivalent of 2 energy saving light bulbs.

Now it comes with Linpus linux, a distro that I think I have heard of. But the fact I questioned it means it's no good. So a quick USB install later I have Ubuntu 10.04. I was tempted with the server edition but I thought I would stick with desktop now just to get everything running and maybe try a fresh install of server edition later.
<h4>We begin</h4>
So a few nagging problems first with graphics and then sound. So it appears that the generic graphics drivers are quite good but the revo does have some dedicated linux drivers to help use all the juice the new ION chip has to offer and since I have some 1080p movies this is a must as the Atom chips just won't cut it. So after a lengthy system update process I can get the graphics drivers. A simple trip to System --&gt; Administration --&gt; Hardware drivers picked up the problem and downloaded the relevant drivers.

Most of the rest was done by following <a href="http://www.greenhughes.com/content/how-install-ubuntu-910-and-boxee-beta-acer-aspire-revo-including-64-bit-option?page=1">Liam Green-Hughes blog</a> post on his install with 9.10. So that was sound and graphics sorted. I ran mplayer with my sample movie but still couldn't it to play properly, it was stuttering all over the place. Some more searching later revealed a few things. One was that I needed to explicitly  tell the player to use the right driver, I had to download a package libvdpau1 I used Synaptic Manager) then point mplayer to it. More frustration, other forums pointed to smplayer (basically a gui front end for mplayer) I thought what the hell, so I installed that set the options to use this package for the video output and still no luck. Then I tried mplayer with the relevant option to use that package and no such luck. I then installed nvidia-glx-(something, I can't remember it was in a forum somewhere) package but still no dice.  After a while I realised you had to log out and log back in for graphics changes to take effect, essentially restart X. So I did that and then tried smplayer and it worked like a charm (interestingly I couldn't get mplayer command line to work :-S ). I removed the nvidia-glx-180 package and restarted X and it still worked in smplayer, so I am happy.

Next xbmc....
