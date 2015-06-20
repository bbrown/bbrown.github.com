---
layout: post
title: Good Article
date: '2003-05-18 18:59:19 -0700'
mt_id: 213
blog_id: 1
post_id: 213
basename: good-article
categories:
- programming
---
<br />There's a good article on <a href="http://www-106.ibm.com/developerworks/java/library/j-jtp04223.html?ca=dgr-lnxw01JavaUrbanLegends">Java performance myths</a> at <a href="http://www-106.ibm.com/developerworks/">developerWorks</a>. <a href="http://slashdot.org/">Slashdot</a> provides some <a href="http://developers.slashdot.org/article.pl?sid=03/05/17/175255&amp;mode=thread&amp;tid=126&amp;tid=156&amp;tid=108">interesting context</a>.<br /><br />My favorite is myth #3 that immutable objects are performance killers. I was just having a discussion with a developer from our <a href="http://www.corillian.com/">online banking system vendor</a> and he mentioned that some of the code in our existing implementation uses straight-out string objects instead of string buffers. I realize that <acronym title="Visual Basic">VB</acronym> and VBScript is a little different from Java, especially since very little of the language seems to be optimized and string concatenation does seem expensive.<br /><br />It's always worth emphasizing design before performance. I'll admit that I'm guilty of it on occasion as well, but articles like this chip away at that optimization part of my brain. Some day I hope to not even think about performance until 1.0b!<br /><br /><br />
