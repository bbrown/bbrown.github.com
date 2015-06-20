---
layout: post
title: Can't Pull the Rug Out From Under Yourself
date: '2006-12-21 14:50:00 -0700'
mt_id: 1173
blog_id: 1
post_id: 1173
basename: cant-pull-the-rug-out-from-under-yourself
categories:
- future-reference
- net-development
---
<p>
I found another big gotcha in .NET today. When iterating over a Hashtable, you might want to change something within that Hashtable, like say change or clear out a value. Ain't gonna happen, buddy. Nice big runtime exception: <code>Collection was modified; enumeration operation may not execute</code>.
</p>
<p>
I got it the first time and I slapped my forehead&#x2014;figuratively, of course, as I'm not in the habit of self-flagellation. So I did what I always do. *sigh* I got clever. I thought that I could obviate the problem by enumerating through the <code>Hashtable.Keys</code> collection and make my changes that-a-way.
</p>
<p>
Again, no dice. I'm not entirely sure how changing the value of a Hashtable key while looping over a collection of keys is affecting the underlying Hashtable. But I think it has something to do with the CLR iterating over the Keys collection by reference rather than by value.
</p>
<p>
The answer, after some Googling, is to split the operation into two phases: storing the keys to be changed in another collection and then looping over that second store to actually modify the values or do what-have-you. It's decidedly not as elegant as say creating an <a href="http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dncscol/html/csharp01212002.asp">isolating enumeration class</a>, but I've got work to do.
</p>
