---
layout: post
title:  "Basic Git Commands"
categories: Web Design Tutorials
description: Common git commands for pushing content to my Github account
---

Generally, I don't use the command line to interact with my version controlled client accounts. In most cases, I prefer to use [Tower](https://www.git-tower.com), a great Git client for Mac and Windows but in the case of gbradhopkins.com, I decided to use the command line as a way of becoming more familiar with it. Below are the basic commands that I use to push content to my Github account. 

These are the steps for commiting new or updated content to my [Github account](https://github.com/firebrandmedia). As I use Git more, hopefully these will become muscle memory and I'll no longer need this document. Until then…

## Commands for pushing content

After creating or editing a file, run the following commands in the Terminal.

`git status`

This is an optional command. It simply shows what has changed and results in something like this:

```
modified:   _includes/head.html
modified:   _sass/_gbradhopkins.scss
modified:   css/main.scss
```
We can then review the list of changes and if satisfied, move to the next step.

`git add .`

`git commit -m 'Commit message here'`

After adding our commit message and hitting enter, we receive a message indicating what we've done (or are about to do).

```
[gh-pages c5656de] git article update
 1 file changed, 3 insertions(+), 1 deletion(-)
 ```

`git push `

That's it. All done. The files are now commited to the repository that we've been working in.

Next up, how to access that repository from another computer to continue working on it.