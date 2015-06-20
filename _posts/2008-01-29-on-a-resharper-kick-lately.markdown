---
layout: post
title: On a ReSharper Kick Lately
date: '2008-01-29 15:07:46 -0700'
mt_id: 1255
blog_id: 1
post_id: 1255
basename: on-a-resharper-kick-lately
categories:
- net-development
---
<p>I've been tweaking <a href="http://www.jetbrains.com/resharper/">ReSharper</a> something fierce lately. I've talked <a href="http://bbrown.info/2005/07/21/looking-sharper-2.aspx">about it</a> <a href="http://bbrown.info/2006/05/23/get-thee-to-thy-browser-and-download.aspx">before</a>, but some day I'm going to write up all the things that make me love that little Visual Studio add-in. I know some suggest you should <a title="Defaults are great, but how often are you working on a machine that is not yours?" href="http://www.codinghorror.com/blog/archives/000290.html">learn to love defaults</a>, but others argue for <a href="http://pragmaticprogrammer.com/the-pragmatic-programmer/extracts/tips">knowing thy editor</a>.</p> <p>One of my favorite features are <a href="http://www.jetbrains.com/resharper/features/codeTemplate.html">live templates</a>. If you can get <a href="http://joeydotnet.com/blog/archive/2006/12/07/11.aspx">used to them</a>, your productivity will soar since your hands will never leave the keyboard. I have gotten used to them and regularly create new ones when I find myself repeating.</p> <p>Today I created an awesome template for doing <code>StringBuilder.Append</code>s. Now all I type is <code>sb</code> and it expands to <code>actualStringBuilderObject.Append("MESSAGE");</code> with the cursor replacing the "MESSAGE" string and the enter key dropping the cursor off at the end of the line. That description doesn't do the template justice, so just make one using the screenshot below:</p> <p style="text-align:center;"><a href="http://bbrown.info/images/34-25/resharper-stringbuilder-live-template-large_2.png" target="_blank"><img style="border:0 none;" alt="Screenshot of ReSharper Live Template dialog" src="http://bbrown.info/images/34-25/resharper-stringbuilder-live-template-large_thumb.png" border="0" height="244" width="230"/></a> </p> <p>You can get to that dialog by clicking ReSharper &gt; Options &gt; Live Templates and then clicking on the + icon.</p>
