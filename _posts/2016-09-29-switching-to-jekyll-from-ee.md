---
layout: post
title:  "Moving gbradhopkins.com from ExpressionEngine to Jekyll"
categories: Web Design Tutorials
description: Thoughts, links and resources as I switch my personal site from EECMS to Jekyll
---

Looking for an opportunity to play around with Git, Markdown and Jekyll, I have decided to move my site from [ExpressionEngine (EECMS)](http://ellislab.com/expressionengine) - which I love and use on most projects - to [Jekyll](http://jekyllrb.com), a static site generator.

## Static Site Generator?

*What is a static site generator and why would you want to use it?* I'm glad you asked.

A static site generator takes a template directory containing raw text files in various formats, runs it through a converter and a renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server.

A static website doesn't require a database which can increase security and will typically load faster. Although, there are plenty of ways to slow down a static site.

## Caveat

Back in 2015, [I gave a talk on creating websites with Jekyll.](http://epwebtech.com/events/2015/08/12/getting-started-with-jekyll.html) My first caveat was that you need to use the terminal / command line interface (CLI). I knew that would be a dealbreaker for some people but if you can overcome your fear of the terminal, using Jekyll can help make you more comfortable with a CLI.

## Installing Jekyll

For the full installation guide, [check out the Jekyll install documentation](https://jekyllrb.com/docs/installation/). Here is my quick overview.

Using the terminal / command line, run the following command to install Jekyll.

`gem install jekyll`

If you run into an error, first make sure that you have Xcode installed. If Xcode is installed, try installing Jekyll again with this command (which will require that you supply the password for your computer).

`sudo gem install jekyll`

## Exporting Entries

In addition to creating a blog in Jekyll, I wanted to move all/some of my posts from EECMS.

Here is the template that I used to export all of my entries from EECMS to a single HTML file. This file exports each entry as a field in a table. Because most of my entries were old and no longer relevant, I am using this as more of a time capsule so that in the future I can look back at what I wrote.

```
<?php
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
```

## Exporting Individual Entries

For most, exporting a single file that includes every entry is probably not practical and, honestly if I could figure it out, I wanted to maintain the entries as individual files as well.

The thing I love most about ExpressionEngine is the ability to format and display your data however you need. Using two templates I was able to:

- List all of my entries with the naming convention that Jekyll requires - "Year-Month-Day-Title.md"
- Click a link to download each entry formatted for Jekyll with the frontmatter already in place - layout, title, categories, date, custom image field for hero images

<strong>List of Entries Template</strong>

This is a very simple template but it gets the job done, creating a list of entries with links to download the individual files.

```
<ul>
{exp:channel:entries channel="tutorials|reviews" dynamic="off" disable="member_data|pagination"}
<li><a href="{title_permalink='exports/post'}" target="blank">{entry_date format='%Y-%m-%d'}-{url_title}.md</a></li>
{/exp:channel:entries}
</ul>
```

<strong>Entry Download Template</strong>

Clicking on the entry link from the list above, fires the template below which initiates the download process. If you are trying to use this template, make sure you turn on 'Allow PHP' in the template preferences in EE.

```
{exp:channel:entries channel="tutorials|reviews" disable="member_data|pagination"}
<?php
header("Content-type: text/markdown; charset=UTF-8");
header("Content-Disposition: attachment; filename={entry_date format='%Y-%m-%d'}-{url_title}.md");
header("Pragma: no-cache");
header("Expires: 0");
?>
---
layout: post
title:  "{title}"
date:   {entry_date format='%Y-%m-%d %H-%i-%s'} -0500
categories: {categories}{category_name}{/categories}
{if tutorial_hero_image}image: {tutorial_hero_image}{/if}
{if review_hero_image}image: {review_hero_image}{/if}
---

{exp:marker:tomarkdown}
{tutorial_hero_image}

{tutorial_body}

{tutorial_image}

{review_body}
{/exp:marker:tomarkdown}

{/exp:channel:entries}
```

The one thing I couldn't figure out was how to download the file with the .md file extension. Using the above code downloads a file with .md.html as the file extension. I simply used a renaming app to batch rename all of the files to .md.

## Links of note

- [Exporting entries from EECMS to an HTML file](https://expressionengine.stackexchange.com/questions/515/what-is-the-best-method-for-exporting-channel-entries-as-a-spreadsheet)
- [Marker Add-on for EECMS to convert entries to Markdown](https://devot-ee.com/add-ons/marker)
- [Formatting Markdown in Jekyll](https://milanaryal.com/writing-and-formatting-with-markdown/)
- [Git Reference Guide](http://gitref.org/basic/#add) - Basics of commiting and pushing content.
- [Jekyll Links and Resources](http://epwebtech.com/blog/2015/08/17/jekyll-resources-and-links.html) - A list of resources that I pulled together for a talk that I gave back in 2015.
- [Publishing a Jekyll Site on Gituhub](http://epwebtech.com/blog/2015/08/18/publishing-site-to-github.html) - Notes on publishing a Jekyll site on Github from the same talk.