---
layout: post
title:  "Moving gbradhopkins.com from ExpressionEngine to Jekyll"
categories: Web Design Tutorials
description: Thoughts, links and resources as I switch my personal site from EECMS to Jekyll
---

Looking for an opportunity to play around with Git, Markdown and Jekyll, I have decided to move [this site](http://gbradhopkins.com) from [ExpressionEngine (EECMS)](http://ellislab.com/expressionengine) - which I love and use on most projects - to [Jekyll](http://jekyllrb.com), a static site generator.

## Static Site Generator?

*What is a static site generator and why would you want to use it?* I'm glad you asked. 

A static site generator takes a template directory containing raw text files in various formats, runs it through a converter and a renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server, or even for free using Github Pages (more on that later).

A static website doesn't require a database, which can increase security and will typically load faster. *Although, there are plenty of ways to slow down a static site.*

In addition to increased security and speed, Jekyll also creates a local server for testing purposes. Every time you make a change to a file or post, you can preview the change locally before pushing the site live. This is a great time saver, especially when testing a responsive design or a blog post.

Finally, if you are using Jekyll, and have a Github account, you can host your site for free using [Github Pages](https://pages.github.com). You can even use your own domain - as I'm doing here. 

Of course, there are some restrictions, one being that many of the Jekyll plugins that are available can't be used because Github runs Jekyll in safe mode. Another restriction that I found is the lack of a .htaccess file, meaning that I couldn't redirect my pages from their old URL to their new URL. One way that I tried to overcome this was by creating a sitemap and submitting it to Google, using the Google Search Console (formerly Webmaster Tools).

## Caveat

Besides the restrictions mentioned above, there is another major caveat regarding the usage of Jekyll. 

**The Command Line**

Back in 2015, [I gave a talk on creating websites with Jekyll.](http://epwebtech.com/events/2015/08/12/getting-started-with-jekyll.html) My first caveat was that you need to use the terminal / command line interface (CLI). I knew that would be a dealbreaker for some people but, if you can overcome your fear of the terminal, using Jekyll can help make you more comfortable with a CLI.

Now that we've got the why and why not out of the way, let's get started.

## Installing Jekyll on a Mac

For the full installation guide, [check out the Jekyll install documentation](https://jekyllrb.com/docs/installation/). Here is my quick overview.

First make sure that you have [Xcode](https://itunes.apple.com/us/app/xcode/id497799835) installed. It's a free download from the app store.

Using the terminal / command line, run the following command to install Jekyll.

`gem install jekyll`

If you run into an error, first make sure that you have Xcode installed. If Xcode is installed, try installing Jekyll again with this command (which will require that you supply the password for your computer).

`sudo gem install jekyll`

If everything goes well, Jekyll will now be installed on your computer and you can start using it.

I'm not going to get into the 'how' of designing a site with Jekyll. That may be a later blog entry but for now I'm more concerned with the transition from ExpressionEngine to Jekyll.

## Bulk Entry Export

In addition to creating a blog in Jekyll, I wanted to move all/some of my posts from EECMS.

I'll admit, what follows is a bit of a cheat. I wanted to export my entries from EECMS to Jekyll but I just couldn't figure out how without putting in a bunch of time that I didn't have. So, instead, I came up with the following solution that I used to export _ALL_ of my entries from EECMS to a single HTML file. This file exports each entry as a field in a table. Because most of my entries were old and no longer relevant, I was satisfied to use this as more of a time capsule, or archive, so that in the future I can look back at what I wrote.

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

- List all of my entries with the naming convention that Jekyll requires - "Year-Month-Day-Title.md" - I was set on using Markdown so the .md format was important.
- Click a link to download each entry formatted for Jekyll with the [front matter](https://pages.github.com) already in place - layout, title, categories, date, custom image field for hero images.

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

I then dropped the files in my _posts directory, rebuilt my site and pushed the changes to my Github account.

## Links of note

- [Exporting entries from EECMS to an HTML file](https://expressionengine.stackexchange.com/questions/515/what-is-the-best-method-for-exporting-channel-entries-as-a-spreadsheet)
- [Marker Add-on for EECMS to convert entries to Markdown](https://devot-ee.com/add-ons/marker)
- [Formatting Markdown in Jekyll](https://milanaryal.com/writing-and-formatting-with-markdown/)
- [Git Reference Guide](http://gitref.org/basic/#add) - Basics of commiting and pushing content.
- [Jekyll Links and Resources](http://epwebtech.com/blog/2015/08/17/jekyll-resources-and-links.html) - A list of resources that I pulled together for a talk that I gave back in 2015.
- [Publishing a Jekyll Site on Gituhub](http://epwebtech.com/blog/2015/08/18/publishing-site-to-github.html) - Notes on publishing a Jekyll site on Github from the same talk.
- [Creating Jekyll Archives with using Plugins](http://reyhan.org/2013/03/jekyll-archive-without-plugins.html) - A great snippet of code that allows you to list your entires by year and date. You can view [my site archives template](http://gbradhopkins.com/archive.html) that is based on this code.