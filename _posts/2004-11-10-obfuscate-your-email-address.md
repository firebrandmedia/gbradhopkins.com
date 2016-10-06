<div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Notice</p>
<p>Message:  Undefined offset: 0</p>
<p>Filename: marker/markdownify_extra.php</p>
<p>Line Number: 288</p>

</div><div style="border:1px solid #990000;padding-left:20px;margin:0 0 10px 0;">

<h4>A PHP Error was encountered</h4>

<p>Severity: Warning</p>
<p>Message:  call_user_func() expects parameter 1 to be a valid callback, class 'Markdownify_Extra' does not have a method 'flushStacked_ul'</p>
<p>Filename: marker/markdownify.php</p>
<p>Line Number: 392</p>

</div>---
layout: post
title:  "Obfuscate Your Email Address"
date:   2004-11-10 15-49-50 -0500
categories: Web Design Tutorials
---

Email Obfuscating? What the heck is email obfuscating and how can it help me avoid SPAM in my inbox?

Obfuscate means : To make so confused or opaque as to be difficult to perceive or understand [[dictionary.com][1]].  
When you obfuscate your email address on a web page you make it hard for a spider to harvest it. Spider? Harvest? Spiders are programs that work their way around the internet harvesting (collecting) information. Some spiders, like search engine spiders, are good. Others, like email spiders (also called spambots) are bad.

  
  


Email spiders scour the internet looking for one thing; Email Addresses. When they find one, they add it to their list. That list eventually becomes part of some CD-ROM that is sold to Spammers. The Spammer then uses that CD-ROM to flood your in box with junk email.

  
  


The question is "How can we protect our email address while maintaining the ability to interact with our visitors?"

  
  


The Answer: Obfuscate your email address. In this tutorial I’ll give you various resources for combatting SPAM.

  
  


To Javascript or not to Javascript, that is the question.

  
  


There are basically two different ways of obfuscating your email address. One is to insert some Javascript code in place of your email, the other is to use plain text that converts your email address into a series of numeric encodings.

  
  


Javascript: Javascript is the more secure of the two methods because spiders are unable to process the script that contains your email address. The only downside to Javascript is that old (primitive) browsers or those with Javascript turned off will not have access to your email address. From what I’ve seen and heard somewhere between 10 and 20% of users will not have Javascript capable browsers (or they will have it turned off).

  
  


Javascript Email Obfuscation Sites [Both of these site will help you generate the Javascript that you will then paste into the HTML of your page.]:

  
  


  
*   [SPAM Proofing Your Web Site : evolt.org][2]  
    *   [Heal Your Church Web Site Anti-spam Email Obfuscator][3]  
        </ul>
          
          
        
        
        Sample Javascript Code created with the Heal Your Church Web Site Obfuscator:
        
          
          
        
        
          
          
          
          
        | <a href="javascript:var e1=’%6d%61c.%63%6f%6d’,e2=’&#109;&#097;&#105;&#108;&#116;&#111;&#058;%20’, e3=’&#098;%72&#097;%64hopki&#110;&#115;’;var e0=e2+e3+’%40’+e1;(window.location?window.location.replace(e0):document.write(e0));" title="&#069;&#109;&#097;&#105;&#108;&#032;&#065;&#100;&#100;&#114;&#101;&#115;&#115;&#032;&#079;&#098;&#102;&#117;&#115;&#099;&#097;&#116;&#101;&#100;&#032;&#087;&#105;&#116;&#104;&#032;&#074;&#097;&#118;&#097;&#115;&#099;&#114;&#105;&#112;&#116;">&#069;&#109;&#097;&#105;&#108;&#032;&#077;&#101;</a> |
        ||
        
          
          
        
        
        Result of the code:
        
          
          
        
        
          
          
          
          
        | [Email Me][4] |
        ||
        
          
          
        
        
        Plain Text: An easier way to obscure your email address is to use plain text. There are a couple of different methods you can use.
        
          
          
        
        
        One way, which you may have seen while browsing, is to type your email address in a way that users have to type it into the address field before sending you a message. It usually will look something like this:
        
          
          
        
        
          
          
          
          
        | brad at mac dot com |
        ||
        
          
          
        
        
        Keep in mind that this decreases usability a bit because users can no longer just click a link that takes them right to their email program.
        
          
          
        
        
        Another way is to use a program like that found on the [Stop SPAM : Spambot Prevention][5] web site. Using that web site generates the following code which can then be pasted into the HTML of your site.
        
          
          
        
        
          
          
          
          
        | &#98;&#114;&#97;&#100;&#104;&#111;&#112;&#107;&#105;&#110;&#115;&#64;&#109;&#97;&#99;&#46;&#99;&#111;&#109; |
        ||
        
          
          
        
        
        Result of the code:
        
          
          
        
        
          
          
          
          
        | bradhopkins@mac.com |
        ||
        
          
          
        
        
        Finally, you could use the Email Obfuscator at the [Alicorna.com][6] web site. This is also a plain text generator but unlike the Stop SPAM site, Alicorna’s code also adds the mailto link so the email address is a clickable link.
        
          
          
        
        
        Sample Code ([Alicorna.com][6])
        
          
          
        
        
          
          
          
          
        | <a href="mailto:&#98;&#114;a&#100;h&#111;&#112;k&#105;&#110;&#115;&#64;m&#97;&#99;.&#99;&#111;&#109;">&#98;&#114;&#97;&#100;&#104;&#111;p&#107;&#105;n&#115;&#64;&#109;&#97;&#99;.&#99;&#111;&#109;</a> |
        ||
        
          
          
        
        
        Result of the code:
        
          
          
        
        
          
          
          
          
        | [bradhopkins@mac.com][7] |
        ||
        
          
          
        
        
        All of these methods will work to some degree. You have to judge which will work best for you. With SPAM as prevalent as it is, you have to be diligent when it comes to guarding that email address.
        
          
          
        
        
          
        *   [Happy spamiversary : CNET News.com][8]  
            *   [SPAM Proofing Your Web Site : evolt.org][2]  
                *   [Stop SPAM : Spambot Prevention : safeemail.org][5]  
                    *   [Heal Your Church Web Site Anti-spam Email Obfuscator][3]  
                        *   [Email Obfuscator : Alicorna.com][6]  
                            </ul></p>

 [1]: http://dictionary.reference.com/search?q=obfuscate
 [2]: http://www.evolt.org/article/Spam_Proofing_Your_Website/20/41849/index.html
 [3]: http://www.healyourchurchwebsite.com/obfuscator/
 [4]: javascript:var e1='%6d%61c.%63%6f%6d',e2='mailto:%20', e3='b%72a%64hopkins';var e0=e2+e3+'%40'+e1;(window.location?window.location.replace(e0):document.write(e0)); "Email Address Obfuscated With Javascript"
 [5]: http://www.safeemail.org/
 [6]: http://alicorna.com/cgi/obfuscator.cgi
 [7]: mailto:%26#98;%26#114;a%26#100;h%26#111;%26#112;k%26#105;%26#110;%26#115;%26#64;m%26#97;%26#99;.%26#99;%26#111;%26#109;
 [8]: http://news.com.com/2100-1024-5189340.html?tag=cd.top

