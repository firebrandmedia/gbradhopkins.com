---
layout: post
title:  "Only certain keys working on your Mac keyboard? This may be the solution."
categories: software
description: Only certain keys working on your keyboard? Command and Tab working while others aren't? Here is the solution.
---

My daughter decided to confound me this afternoon by hitting the option key 5 times on our MacMini. She did this accidentally, but once she did, the keyboard no longer worked in its normal way. Unbeknownst to me, she enabled Mouse Keys.

## What Are Mouse Keys?

Mouse Keys allow you to use your keyboard to move your pointer around the screen instead of a mouse or trackpad.

>"When Mouse Keys is enabled with one of these keyboards, you can use the keys 7,8,9, U, I, O, J, K, L, M, and '.' (period) to control movement of the mouse pointer and mouse clicking, but other numbers, letters, and keys cannot be used. (Keyboards with no numeric keypad or Num Lock key include: Apple Wireless Keyboard (2007), the built-in keyboard on MacBook (Late 2007) or newer, MacBook Air, or MacBook Pro (Early 2008), or newer.) The following keys will continue to operate normally when Mouse Keys is enabled: Esc, Function keys, Eject, Delete, Tab, Shift, fn, Control, Option, Command, and the arrow keys.

I had no idea such a feature existed and was racking my brain to figure out what the issue was. I restarted several times, disconnected the keyboard (bluetooth), zapped the [NVRAM](https://support.apple.com/en-us/HT204063) and tried various other types of voodoo to no avail. Finally, I stumbled upon an article from [2009 on CNet](https://www.cnet.com/news/mac-keyboard-not-working-mouse-keys-may-be-activated/) which described my issue.

## Enabline / Disabling Mouse Keys

If you have no intention of ever using Mouse Keys, I'd recommend disabling it altogether. Not surprisingly, the option is found under Accessibility, which seems to be a treasure trove of goodies to enhance (or, impair) your computer.

!["Accessibility Menu Screen Capture"](/images/mouse-keys-1.png "Accessibility Menu")

Once you are in the Accessibility system preference pane, click on 'Mouse & Trackpad' to show the check-box for enabling / disabling Mouse Keys.

!["Mouse & Trackpad Preference Pane Screen Capture"](/images/mouse-keys-2.png "Mouse & Trackpad Preference Pane Screen Capture")

Ticking the checkbox enables Mouse Keys and reneders your keyboard otherwise useless. To set the option for enabling by tapping 'option' 5 times, click on the options button.

!["Mouse & Trackpad Preference Pane Screen Capture"](/images/mouse-keys-3.png "Mouse & Trackpad Preference Pane Screen Capture")

It's a bit disappointing that they don't actually indicate the keys to use to move the pointer around the screen. Without the guide of which keys to use, this feature seems less helpful than it could be.