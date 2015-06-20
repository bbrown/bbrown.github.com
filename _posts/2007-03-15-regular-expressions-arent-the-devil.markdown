---
layout: post
title: Regular Expressions Aren't the Devil
date: '2007-03-15 15:02:00 -0700'
mt_id: 1223
blog_id: 1
post_id: 1223
basename: regular-expressions-arent-the-devil
categories:
- programming
- net-development
---
<p>
I love regular expressions. Okay, I love the challenge of crafting regular expressions. I do not enjoy reading regular expressions that I have not created or, really, even the ones I do create. But give me a problem and tell me to make a regular expression to match things and I am all over it.
</p>
<p>
A co-worker wanted a regular expression to turn unlinked URLs in text into HTML links and to correct linked URLs that lacked a protocol into valid URLs. In other words, if "www.google.com" appeared in some text, it needed to be replaced with <code>&lt;a href="http://www.google.com/"&gt;www.google.com&lt;/a&gt;</code> and <code>&lt;a href="www.google.com"&gt;some link text&lt;a&gt;</code> needed to turn into <code>&lt;a href="<strong>http://</strong>www.google.com"&gt;some link text&lt;a&gt;</code>
</p>
<p>
My first pass was a monster regular expression that handled both situations but I couldn't get the replacement string to account for the fact that there was already link text in the invalid URL example. And I couldn't adequately cover the situation where there were attributes before the <code>href</code> attribute. So scrap that one.
</p>
<p>
This is what I came up with after separating it into two replacement passes. I share it with you both as a testament to my regular expression abilities (good or bad, you decide) and because this situation seems like one that might come up pretty frequently.
</p>
<table>
<tr>
<th>Regular expression</th>
<th>Replacement string</th>
</tr>
<tr>
<td><code>(?&lt;=\s|^)(?&lt;domain&gt;www\.[^\s]+)(?=\s)<br />|(?&lt;=\s)(?&lt;protocol&gt;http[s]?://){1}<br />(?&lt;domain&gt;(www)?\.?[^\s]+)(?=\s)</code></td>
<td><code>&lt;a href="http://${domain}"&gt;${domain}&lt;/a&gt;</code></td>
</tr>
<tr>
<td><code>href="(?&lt;domain&gt;www\.[^"]+)"</code></td>
<td><code>href="http://${domain}"</code></td>
</tr>
</table>
