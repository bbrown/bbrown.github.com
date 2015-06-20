---
layout: post
title: Managing Content
date: '2007-10-27 00:50:00 -0700'
mt_id: 1245
blog_id: 1
post_id: 1245
basename: managing-content
categories:
- web-tech
- net-development
---
<p>So I'm looking for the best open-source .NET CMS out there. Here's what I've found for options:</p><ul><li><a href="http://www.cuyahoga-project.org/">Cuyahoga</a></li><li><a href="http://umbraco.org/">Umbraco</a></li><li><a href="http://www.rainbowportal.net/">Rainbow Portal</a></li><li><a href="http://www.axcms.net/">AxCMS.net</a></li><li><a href="http://www.sharpcms.net/">Sharp CMS</a></li><li><a href="http://www.mojoportal.com/">mojoPortal</a></li></ul><p>This is the part that I really dread: deciding amongst competing technologies. Each of them has features that I like and some of them even have user interfaces that I prefer. But then, at the same time, you have to look at the codebase and decide which is the one that is extensible, maintainable, and understandable. And the two assessments rarely overlap.</p><p>In this situation, there is no overlap. Rainbow Portal has probably the best user interface, but it's development seems completely stalled and the codebase is, well, terrible. Cuyahoga has an okay user interface (from what I can surmise given the lack of a demo site), an okay codebase (no unit tests, NHibernate pain, fairly straightforward separation of modules from core code), and decent development cycles but a rather <a href="http://www.cuyahoga-project.org/home/forum.aspx?g=topics&amp;f=8">lackluster slate of sites using it</a>. Umbraco has an odd codebase (I found it very confusing at least), unknown user interface (really hard to pin it down from the code), good development cycles, and a pathetic <a href="http://umbraco.org/tour/sites-running-umbraco">slate of sites</a>. The rest of them I didn't like for one reason or another.</p><p>Ultimately I have to pick based on which CMS has the codebase that I can live with most. If the user interface isn't that compelling, I can make it better if I have source that I'm comfortable with. Plus, I'm going to be extending the hell out of it so it's got to be robust enough that I'm not fighting the tool to expand and create new applications or modules.</p><p>Cuyahoga seems to be it. I just wish I could be more satisfied with the choice; I guess that couldn't happen unless I was rolling my own.</p>
