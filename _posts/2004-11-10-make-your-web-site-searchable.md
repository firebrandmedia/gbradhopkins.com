<div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div>---
layout: post
title:  "Make your web site searchable"
date:   2004-11-10 11-46-22 -0500
categories: Web Design Tutorials
---

The ability to search a site is probably one of the most useful features you can add to your site. Especially if your site has a number of pages. If you have a very basic site with a handful of pages then you probably don’t want to even bother with it.

There are a number of free services that help you to quickly and efficiently add search capability to your site. The one that I prefer and am going to use is by [Atomz.com][1]. It is free, has no banners or advertising and can be set to index (scan your site for updated files) your site at intervals that you determine. A very nice feature.

Like all online services you will have to sign up for an account. This process involves you providing minimal information and is very quick.

You will then have to set up an account for the site you wish to make searchable. This can be done at the ‘Accounts’ page. You will need to have the URL that your site resides at [http://homepage.mac.com/bradhopkins is my URL], a title for the site, a category to describe the site and your time zone. This completes the account set up.

Another nice feature provided by [Atomz.com][1] is that you can set up searches for multiple sites and manage all of them from a single page.  


Your next step is to select ‘HTML’ from the list of choices. Here you have two options [1] standard search : the user puts in keywords to search for, and [2] advanced: the user provides information like keywords, date modified, where the file should reside, etc. Either way the process is the same [but the code will be different].

Once you decide which search you like better [I like standard for its simplicity] then you simply copy the code straight from the page.

| *<!—Atomz Search HTML for g.Brad.hopkins—><form method="get" action="http://search.atomz.com/search/"><input size=15 name="sp-q"><br>  
<input type=submit value="Search"><input type=hidden name="sp-a" value="sp1000190a"></form>  
* |
||

This code will then be pasted directly into your web page. Some HTML editors have trouble pasting HTML code from other applications. If the HTML code appears on your web page as text, then copy-and-paste from this page to a simple text editor, then copy-and-paste again from the simple text editor to your HTML editor. (You can use "notepad" on Windows or "Simple Text" on a Macintosh as a simple text editor.)

If the text box is too wide for your design, just reduce its width by changing the size parameter of the "sp-q" input tag in the HTML code for your search form.

Once you have pasted the code into your site you then have to tell atomz.com to index your site. You can set it up to only index on your command, or you can have it index on a schedule. I chose on command and will probably go back later and set up a schedule for indexing.

Simply select ‘Full Index’ and it will tell you when your site was last craweled [indexed] and how many pages were indexed. You will see a button down the page that says ‘index now’ and you click that and it begins indexing [as indicated by the countdown from 20 to 0].

Upon completion of the indexing it will say ‘click here now’. At that point you are done and your site is now searchable. If you get a result of 0 pages then you may want to check to be sure that you typed your URL correctly.

 [1]: http://www.atomz.com

