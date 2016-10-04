---
layout: post
title:  "Git Commit Workflow"
categories: Web Design Tutorials
description: Common git commands for pushing content to my Github account
---

I'm writing this down for me. Not you.

These are the steps for commiting new or updated content to my [Github account](https://github.com/firebrandmedia). As I use Git more, hopefully these will become muscle memory and I'll no longer need this document. Until then…

## Commands for pushing content

After creating or editing a file, run the following commands in the Terminal.

`git status`

This is an optional command. It simply shows what has changed and results in something like this:

```
	modified:   _includes/head.html
	modified:   _posts/2016-09-29-git-commit-workflow.md
	modified:   _posts/2016-09-29-switching-to-jekyll-from-ee.md
	modified:   _sass/_gbradhopkins.scss
	modified:   _site/internet/tutorials/2008/12/09/recovering-individual-files-from-plesk-backup.html
	modified:   _site/internet/tutorials/2013/04/30/internet-privacy-links.html
	modified:   _site/internet/tutorials/2013/05/17/get-fit-and-help-those-in-need.html
	modified:   _site/mac/tutorials/2012/02/06/toggle-between-tabs-in-safari.html
	modified:   _site/mac/tutorials/2013/04/22/macheist-nanobundle-3.-10-well-spent.html
	modified:   _site/pc/tutorials/2013/06/25/ripping-dvd-to-ipod-video.html
	modified:   _site/web/design/tutorials/2008/12/10/not-seeing-any-google-custom-search-engine-results-in-analytics-heres-the-f.html
	modified:   _site/web/design/tutorials/2016/09/29/git-commit-workflow.html
	modified:   _site/web/design/tutorials/2016/09/29/switching-to-jekyll-from-ee.html
	modified:   css/main.scss
```

`git add .`

`git commit -m 'Commit message here'`

`git push `

That's it. All done.