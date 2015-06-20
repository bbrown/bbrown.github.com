---
layout: post
title: DictionaryBase and Repeaters
date: '2005-07-22 03:51:37 -0700'
mt_id: 971
blog_id: 1
post_id: 971
basename: dictionarybase-and-repeaters
categories:
- net-development
---
<br />I've been struggling to databind a custom collection built off DictionaryBase to a Repeater. In my other custom collections that used CollectionBase, I could just cast the Container.DataItem to the underlying type and access the class's properties. When I tried to do the same thing for my DictionaryBase collection, it kept giving me casting errors.<br /><br />I tried casting the DataItem to the collection itself and using keys and values. The Web wasn't particularly helpful. In explaining it to a coworker, who helpfully <a href="http://c2.com/cgi/wiki?RubberDucking">rubber ducked</a> for me, I realized that I needed to cast the DataItem to a DictionaryEntry and then cast the value of that DictionaryEntry to my underlying type. Duh!<br /><br />Here's the syntax, with any confidential bits removed:<br /><br /><code></code><br /><br /><br />
