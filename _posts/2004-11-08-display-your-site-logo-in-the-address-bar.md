---
layout: post
title:  "Display Your Site Logo in the Address Bar"
date:   2004-11-08 13-59-21 -0500
categories: Web Design Tutorials
---

How do you display your web site logo in the address bar? Use favicon, a bit of code and this tutorial.

What is favicon? Favicon is a custom site logo that can be added to your web site. This logo shows up in the address bar and can add a professional look to your site. See image below. *note - some browsers do not support favicon.*

![][1]

gbradhopkins.com favicon in Netscape 7

Adding favicon to your site is a fairly simple, two step process.

**Create the file** : First, you must create the favicon file. This file has to be a .ico (windows icon) file with dimensions of 16 x 16 pixels. *I used [Graphic Converter][2] (Mac) to create my .ico file but there are many programs available that will do the job (search for .ico at [download.com][3]).* 

**Implementing** : Option 1) If you have root access then you can simply put the .ico file in the root level of your web site. This is the easiest way and will ensure that every page in your site will have the icon. When using this method, the file must be named favicon.ico.

Option 2) If you do not have root access, then you can add a small snippet of code to each page that you would like the icon to be displayed on. 

*<LINK REL="SHORTCUT ICON"  
HREF="/~your_directory/logo.ico">*

Add this code between the <HEAD> and </HEAD> tags of your page, replacing */~your_directory/logo.ico,* with the location and name of your .ico file. Using this method, you can name the file anything you like and can use different files for different sections of your site.

 [1]: http://www.gbradhopkins.com/images/webdesign/favicon/Netscape-screenshot.gif
 [2]: http://www.versiontracker.com/dyn/moreinfo/macosx/11559
 [3]: http://www.download.com

