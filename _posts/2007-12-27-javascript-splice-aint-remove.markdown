---
layout: post
title: Javascript Splice Ain't Remove
date: '2007-12-27 06:00:00 -0700'
mt_id: 1251
blog_id: 1
post_id: 1251
basename: javascript-splice-aint-remove
categories:
- programming
---
<p>I wanted to remove an item from a Javascript array and looked in vain for a remove function. I did find an implementation of <code>remove</code> using the <code>Array.prototype</code> but I just needed a function to get rid of items that matched a specific criterion.</p><p>That's when the trouble started. The splice function&#x2014;calling its <code>array.splice(index, count)</code> variant&#x2014;will indeed remove an item or items from the array (and return an array of the items removed for some reason) but it also closes the void left by the removed item and resizes the array all in one fell swoop. So code like this doesn't work as you'd think:</p><blockquote><code>for (var i = 0; i &lt; array.length; i++)<br />{<br />&#xA0;&#xA0;&#xA0;if (array[i].someParameter == "someValue")<br />&#xA0;&#xA0;&#xA0;{<br />&#xA0;&#xA0;&#xA0;&#xA0;&#xA0;&#xA0;array.splice(i, 1);<br />&#xA0;&#xA0;&#xA0;}<br />}<br /></code></blockquote><p>Since <code>array.length</code> changes with each removal, this code will end up missing some items because it will end too quickly. In the interest of saving future Googling, frustrated Javascripters, here's how I solved the issue:</p><blockquote><code>for (var i = array.length - 1; i &gt;= 0; i--)<br />{<br />&#xA0;&#xA0;&#xA0;if (array[i].someParameter == "someValue")<br />&#xA0;&#xA0;&#xA0;{<br />&#xA0;&#xA0;&#xA0;&#xA0;&#xA0;&#xA0;array.splice(i, 1);<br />&#xA0;&#xA0;&#xA0;}<br />}<br /></code></blockquote><p>By starting the loop from the top of the array and working backwards, item removals and the dynamic resizing have no effect. If anyone has a better way, I'm all ears. Well, eyes.</p>
