---
layout: post
title:  "Create an RSS Feed for Your Web Site"
date:   2005-11-05 08-50-54 -0500
categories: Web Design Tutorials
---

<p>Anyone with a web page knows that no matter how good your web site is, it's no good unless someone sees it. So, to keep readers informed of updates, most sites employ things like mailing lists to keep readers up to date.
In this tutorial I'm going to show you the simple to way to create your own RSS News Feed.</p>

<p>First, what is an RSS news feed? RSS news feeds are used by web sites to share headlines and stories. These feeds can be used by other web sites or by special RSS aggregators. In this example I will show you how to create an RSS news feed.

<p><b>Create Your Own in XML</b> : There are multiple RSS Feed formats (0.91, 1.0 and 2.0) but in this tutorials we will use the simple 0.91 format. Below you will find a link to the code used to create a sample RSS Feed. Feel free to copy and paste the following code into your own text editor.</p>

Sample RSS Code

```
<?xml version="1.0" ?>
<!DOCTYPE rss PUBLIC "-//Netscape Communications//DTD RSS 0.91//EN"
"http://my.netscape.com/publish/formats/rss-0.91.dtd">
<rss version="0.91">
<channel>
<title>gBradhopkins.com </title>
<link>http://www.gbradhopkins.com/ </link>
<description> Educating computer users one click at a time. Tutorials for Mac, PC and Web designers. </description>
<language>en-us </language> <item>
<title> NetNewsWire and RSS Readers :: Review / Tutorial </title>
<link> http://homepage.mac.com/bradhopkins/tutorials/mac/netnewswire/netnewswire.html </link>
<description> In this product review/tutorial for NetNewsWire I show you how you can browse and find updated content on thousands of web sites without the hassle of intrusive advertising or opening a web browser. 5/23/03</description>
</item> <item>
<title> Quickly and Easily Import Cover Art into iTunes 4 </title>
<link> http://gbradhopkins.com/tutorials/mac/iTunes4/album-art/album-art.html </link>
<description> iTunes 4 allows you to import album artwork to go along with your music. In this tutorial I will show you how to use a freeware program called Clutter to make finding and importing Album Artwork as easy as 1, 2…Done. 5/17/03 </description>
</item> <item>
<title> Re-live the days of your youth with Emulation Software </title>
<link> http://gbradhopkins.com/tutorials/mac/emulator/emulated-games.html </link>
<description> Use your Mac and some free software to play old school games like Frogger, Q-Bert, Pac-Man, Super Mario and more. In this tutorial I show you where to get software that emulates Atari, Nintendo, SuperNintendo and other game systems. 5/16/03 </description>
</item>
</channel>
</rss>
```

<p>Looking at the code in the example, you're probably thinking to yourself that it looks a lot like HTML. And you are right. When creating your RSS Feed, there are only a few things that you need to change to make it work. I have highlighted in orange the items that you will need to change to make your own feed.</p>

<p><b>Title, Link, Description</b> : To make the feed work you really only need to change the Title, Link and Description sections of the code. So, let's whip out our handy Text Editor and get started.</p>

<p>The first Title, Link and Description refers to your site. In my feed I have gbradhopkins.com for the title, the actual link to the site and a description of the site itself. This is the information that will be displayed in the news aggregator.</p>

<p>The next section that is changed refers to the individual headline or news story that you are announcing with your feed. So, when you change the Title, Link and Description, each should refer to the individual article. You can then repeat the process for each of the headlines that you would like to add. Make sure that you leave the tags alone and only change the text in the Title, Link and Description sections. Any changed code will cause problems with your feed. When saving your feed, save it as my-<i>feed-name.rss</i>. [ex- My feed is saved as g_brad_hopkins.rss]</p>

<p><b>Advertise Your Feed</b> : Now that you have created a feed, you need to advertise it. One way, is to add a link on your page that says <a href="http://homepage.mac.com/bradhopkins/g_brad_hopkins.rss">RSS FEED</a>, or use the <a href="http://homepage.mac.com/bradhopkins/g_brad_hopkins.rss"><img src="http://www.gbradhopkins.com/images/webdesign/RSS/xml.gif" alt="" width="36" height="14" align="absmiddle" border="0"></a> graphic. This graphic is a standard indicator of an RSS Feed. The graphic or text should link to your .rss file. [mine links to g_brad_hopkins.rss]. To see what an RSS feed looks like when clicked on, click on either the graphic or text link above.</p>

<p>Another way to advertise your feed is to use a web site like <a href="http://www.syndic8.com/suggest_start.php">Syndic8.com</a>. Syndic8.com allows people to enter or suggest feeds that they will include in their database.You can also use Syndic8.com to find other RSS Feeds.</p>

<p><b>Validate the Feed</b> : To make sure that your feed is sea-worthy, use an online RSS Validator like the one at <a href="http://aggregator.userland.com/validator">Userland Software</a>. Simply input the link to your rss file and it will check to see that everything is valid in your code.</p>

<p><b>View the Feed</b> : To view the feed you will need an RSS aggregator. I am using NetNewsWire Lite for MacOS X. For those using Windows, try out <a href="http://www.disobey.com/amphetadesk/">AmphetaDesk</a>. In the image below you can see my feed in the aggregator window.</p>
