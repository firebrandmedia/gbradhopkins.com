---
layout: post
title:  "Recovering Individual Files from Plesk Backup"
date:   2008-12-09 23-29-07 -0500
categories: Internet Tutorials
redirect_from:
  - /internet/tutorial/recovering-individual-files-from-plesk-backup
---

If you host your website on a server that runs Plesk as the Control Panel, and you actually make back-ups of your server, then at some point you are probably going to want to access the files located on the Plesk generated back-up.

With some free software, it’s easier than you think.

If you are a Mac user, then you are no doubt familiar with Stuffit Expander from Smith Micro.  This expander software was generally installed on every Mac for as long as I can remember. I don’t believe it is still part of the standard install but, no worries, it’s a free download (you just have to provide them with your email address).

1. [download and install the Stuffit Expander software][1].
2. Navigate to your local copy of your Plesk Backup file.
3. Right click on the Plesk Backup File and select Open With…  You will now need to navigate to the Stuffit Expander application that you installed in step 1 (you can find it in your Applications folder). 

That’s all there is to it.  Stuffit Expander should now begin decompressing the Plesk Backup file.  You will need to then decompress the individual files that contain your web files.  On mine the files that comprised my website were found in the ‘*domainname.com.httpdocs*’ folder.

## Not a Mac user?

You’re in luck!  Stuffit Expander is also available as a [free download for Windows][2].  There is one caveat for Window’s users - you also need to install Microsoft .Net Framework ([Redirect from Smith Micro to the Microsoft .Net Framework download page][3]).

## Viewing Databasess

As more and more sites are database driven you may also find that you need to view the database that holds your site together.  This is easy also.  Simply open the database file - mine was called directory.mysql - with a text editor (I used [TextWrangler][4]).  You can then browse or search the database file line by line to extract the data you need.

 [1]: http://my.smithmicro.com/mac/stuffit/expander.html
 [2]: http://my.smithmicro.com/win/stuffit/index.html
 [3]: http://my.smithmicro.com/get.net/
 [4]: http://www.barebones.com/products/textwrangler/

