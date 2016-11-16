---
layout: post
title:  "My Five Favorite Alternative Browsers"
categories: software
description: These are my five favorite alternative web browsers
---

I'm a big fan of trying out alternative browsers. In this entry, I'm going to list my five favorite alternative browsers. By alternative, I mean, not Safari, Firefox or Chrome which make up [over 92% of browser usage worldwide](http://www.w3schools.com/browsers/default.asp).

For a long time I was committed to Firefox and then I moved away from it in favor of Safari. As a Mac user, I have found iCloud tabs to be invaluable and while Firefox Sync can replicate this feature, it was a bit late to the game for me. By the time it was available and they had released an iOS app to make it available on all of my devices, I had already switched back to Safari. Additionally, I felt like speed became an issue with Firefox. This may have been a result of excessive [Tab Group](https://addons.mozilla.org/en-US/firefox/addon/tab-groups-panorama/) usage, another feature that I loved on Firefox and probably abused.

I've never been a big fan of Chrome but I do find some of the developer plug-ins available compelling - although most are also available on Firefox as well so if they were such a big deal I could use them in Firefox and be pretty satisfied. I also like the Chrome dev tools but not so much so that I would switch to Chrome from Safari. 

Now that I've outlined my thoughts on Safari, Chrome and Firefox, here are my five favorite alternative browsers.

## Vivaldi

Based on Chromium, I would consider Vivaldi a good general usage web browser. It has some really interesting features and customizations and because it's based on Chromium, all of the Chrome add-ons work with it. My favorite features are the ability to arrange the tabs wherever you like - top, bottom, side. I also like the adaptive title bar that changes color based on the primary color of the website that you are on. Tab stacks, similar to tab groups in Firefox, are another great feature for organizing tabs.

I would consider it more of a general use browser - as opposed to a developer browser - because the dev tools aren't as fully featured as those found in Chrome.

- [Vivaldi](https://vivaldi.com)

## Min

With a name like Min, what would you expect? Min doesn't seem to be made for users of plug-ins, add-ons and developer tools, also known as power users. It's a fast, minimal browser that has been made using open source software with efficiency and power management in mind. Privacy also seems to be a priority as the default search engine is DuckDuckGo and ads and trackers are blocked by default.

Much like Vivaldi, it features an adaptive title bar that changes color based on the primary color of the site that you are visiting.

My primary use of Min is when I need to take a screenshot of a website without all of the browser chrome.

- [Min](https://minbrowser.github.io/min/)

## Fluid Browser

The Fluid Browser is a totally different concept. It acts as more of a picture-in-picture window for the web. Why would you need a PIP display? Tutorial videos? PDF files? Web media? Fluid acts as a secondary window that can display content while you work in your primary browser or application. I know what you're thinking, "I can do that anyway. Just pop open a new window and drag it off to the side." True, but can you adjust the transparency of the window and work through it? I didn't think so.

I think Fluid is great if you are trying to follow along with a tutorial while working in your primary app.

- [Fluid Browser](http://fluidbrowser.com)

## Tor

You've probably heard of Tor even if you don't know exactly what it is. Tor, based on Mozilla, allows you to browse the web anonymously. You may think, "Wait, can't I just open a private window in Chrome / Safari / Firefox?" Yes, but that doesn't necessarily protect your anonymity. Tor protects your anonymity by relaying your requests through their network. 

In the screen capture below, you can see that even using a private window (middle browser window), my IP address and location are readily available. But, by using Tor (bottom window), my IP and location are anonymized.

!["Screen capture showing anonymized IP address using Tor vs a Private Window"](/images/browser-private-ip-tor.png "Screen capture showing anonymized IP address using Tor vs a Private Window")

From the [description on the Tor site](https://www.torproject.org/projects/torbrowser.html.en):

>The Tor software protects you by bouncing your communications around a distributed network of relays run by volunteers all around the world: it prevents somebody watching your Internet connection from learning what sites you visit, it prevents the sites you visit from learning your physical location, and it lets you access sites which are blocked.

I don't have a lot of activities that I want to protect but, I have found that the ability to access sites that are blocked provides a good workaround when your IP address is blocked. Recently, my IP was blocked by my hosting company because I had the wrong password in an email client that kept pinging the server. After enough failed attempts, my IP was blocked so I was no longer able to access any part of the server - CPanel, FTP, WHM. To make matters worse, the hosting company was Site5 - who I would never recommend - and they weren't responding to support requests. So, to circumvent the block, I simply opened the Tor browser and connected to the server that way. It was a bit slower, but it provided the access that I needed. This is a practical example of how someone who doesn't face a tyrranical government can use Tor. I can only image living in an atmosphere where it was critical to my survival.

- [Tor](https://www.torproject.org/projects/torbrowser.html.en)

## Lynx

Finally, Lynx. If you are old enough, you may remember browsing the internet on a text-based browser like Lynx. For me, Lynx is as much nostalgic as anything else. When I was in college, my first experience with the internet was Lynx. That experience was quickly replaced with a Netscape browser. But, much like those that prefer Vinyl to MP3, I get a warm feeling when I browse a site using Lynx.

Lynx runs through a terminal window and the easiest way to use it is to install the [Lynxlet Termlet](http://habilis.net/lynxlet/). Lynxlet allows you to create a browser bookmark that automatically opens the site that you are currently browsing in Lynx.

Why? Assuming you don't have that same warm and fuzzy feeling that I have for text based browsers, why would you want to do this? If you are a web developer, Lynx is a great way to test the accessibility of your website because it only loads text, avoiding images and javascript. It's also a great way to see your site the way a web crawler would.

In the image below, you can see the homepage of this site in the Lynx browser. Plain text is in purple, links are green and links with focus are in yellow. You scroll the page using the up / down arrow keys and you "click" on a link by arrowing down to it and hitting return.

!["Lynx browser window showing gbradhopkins.com homepage"](/images/browser-lynx.png "Lynx browser window showing gbradhopkins.com homepage")

Based on the image above, I can see that my site has navigation issues because the navigation is non-existent. I am using an icon font for the navigation items, and they're not displayed on a text browser so I should expect that they are not accessible.

- [Lynx](http://osxdaily.com/2011/07/26/get-lynx-for-mac-os-x-10-7-lion/)
- [Lynxlet](http://habilis.net/lynxlet/)

## Obligatory Final Thoughts

I feel like this is a great time to experiment with alternative browsers. There seems to be a lot of vibrancy in the browser community. It's work exploring what else is out there. At the very least, it may reinforce your love of a particular browser.
