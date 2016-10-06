---
layout: post
title:  "Network Two Mac&#8217;s via Firewire"
date:   2004-10-02 17-01-27 -0500
categories: Mac Tutorials
---

When connecting two Macs with Firewire built in, most of us use Firewire Target Disk Mode. In this tutorial, I’ll show you how to connect two Mac’s via IP over Firewire.

MacOS X Panther has added the ability to connect two Macs (or a Mac and a PC, I would assume, since IP over 1394 is supported by WindowsXP) over IP via Firewire.

![][1]To get started, open your System Preferences and click on the Network icon. Next, click on Network Port Configurations (in the Show: pull down menu - see above).

You will then click on the new button in the Port Configuration window. A port configuration dialog box will appear. In the Port: pull down menu select ‘Built In Firewire’ (see image below) and then give it a name (Firewire, etc.).![][2]

Next, in the network port configurations window, drag Firewire to the top of the list and click apply now (This ensures the port is assigned an IP address using DHCP). To finish, click Apply Now and close your system preferences.![][3]

Finally, connect your two Mac’s via Firewire and click on the network icon in your finder. Your second Mac should now be available.

 [1]: http://www.gbradhopkins.com/images/mac/ip-over-firewire/show-menu.gif
 [2]: http://www.gbradhopkins.com/images/mac/ip-over-firewire/built-in-firewire.gif
 [3]: http://www.gbradhopkins.com/images/mac/ip-over-firewire/port-config.gif

