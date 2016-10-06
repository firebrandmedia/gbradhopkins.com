---
layout: post
title:  "Increase Widget Security"
date:   2005-05-13 16-14-51 -0500
categories: Mac Tutorials
---

With the addition of Widgets to MacOS 10.4 “Tiger” a potential security problem has arisen. This tutorial, provided by CJ Correnti of C2 Media Group will help increase the security of Widgets.

One simple solution, is obviously to turn off “Open Safe Files” in Safari, but that does make life a bit more difficult, so, for those who want to have their cake and eat it too (at least on this issue) I found it blindingly easy to add what I think should be closer to the default behavior - and it’s not dependent on Safari.

1. Run “Folder Actions Setup” (in the Applications/Applescript folder).  
2. (if it’s not already on) Turn on “Enable Folder Actions”.  
3. Click the (+) button below the folder column to add a folder.  
4. Select ~/Library/Widgets in the dialog that pops up for folder selection.  
5. Then another dialog asks what action to take and presents a list of pre-made scripts.  
6. Select the “add - new item alert.scpt”. (click OK).  
7. Close up the folder actions application - you’re done.

After this, whenever anything gets put in that folder, the system will alert you that something has been placed in your widgets directory and ask if you want to see it. If you weren’t expecting this, say if you visited the zaptastic site and got “drive-by-downloaded” you’ll at least get tipped to the situation and can either examine the contents of the widget (if you’re a geek like me) or trash it without having to dig through anything. You could also go another step and have Applescript check the contents for certain keys within the widget (say looking for preferences that allow full system access) but I think this will suffice for most people until Apple addresses the problem head on.

It’s also not a bad idea to put a watch on some critical system wide folders this way as well, such as /Library/StartupItems and /System/Library/StartupItems to deal with some of the possibilities you mention as problems of applications asking for admin passwords during installs. Obviously this can be taken farther, but it’s a simple start that at least gives people the chance to see what’s going on, and requires very little tech savvy . Also, I am aware of at least a couple other “packaged” applescripts folks have released to do essentially the same thing, but at least with this method I know Apple wrote the script and I did the setup.

