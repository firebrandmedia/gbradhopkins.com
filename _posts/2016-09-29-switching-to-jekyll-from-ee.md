---
layout: post
title:  "Moving gbradhopkins.com from ExpressionEngine to Jekyll"
categories: Web Design Tutorials
description: Thoughts, links and resources as I switch my personal site from EECMS to Jekyll
---

Looking for something with a bit less overhead and an opportunity to play around with Git and Jekyll, I have decided to move my site from [ExpressionEngine](http://ellislab.com/expressionengine) - which I love - to [Jekyll](http://jekyllrb.com).

## Links of note

- [Exporting entries from EECMS to an HTML file](https://expressionengine.stackexchange.com/questions/515/what-is-the-best-method-for-exporting-channel-entries-as-a-spreadsheet)
- [Formatting Markdown in Jekyll](https://milanaryal.com/writing-and-formatting-with-markdown/)
- [Git Reference Guide](http://gitref.org/basic/#add) - Basics of commiting and pushing content.
- [Jekyll Links and Resources](http://epwebtech.com/blog/2015/08/17/jekyll-resources-and-links.html) - A list of resources that I pulled together for a talk that I gave back in 2015.
- [Publishing a Jekyll Site on Gituhub](http://epwebtech.com/blog/2015/08/18/publishing-site-to-github.html) - Notes on publishing a Jekyll site on Github from the same talk.

## Code

Here is the template that I used to export all of my entries from EECMS to an HTML file. This file exports each entry as a field in a table.

`<?php
    header("Content-type: application/vnd.ms-excel");
header("Content-Disposition: attachment; filename=gbradhopkins-entries-exports.xls");
header("Pragma: no-cache");
header("Expires: 0");
?>
<table>
<tbody>
{exp:channel:entries channel='tutorials' limit='500' disable="categories|member_data|pagination|trackbacks"}
    <tr>
	    <td valign="top">{title}</td>
            <td>{tutorial_body}</td><td>{tutorial_image}</td><td>{tutorial_hero_image}</td>
    </tr>
{/exp:channel:entries}
</tbody>
`