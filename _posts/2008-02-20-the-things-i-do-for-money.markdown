---
layout: post
title: The Things I Do For Money
date: '2008-02-20 23:32:59 -0700'
mt_id: 1261
blog_id: 1
post_id: 1261
basename: the-things-i-do-for-money
categories:
- personal
- net-development
---
<p>
Pardon me while I vent for a few minutes. I'm doing some contract development work for a non-profit&#x2014;cleared long ago through my company's legal team to make sure that I wasn't running afoul of my non-compete clause&#x2014;and to say that the conditions are sub-par is to put it mildly.
</p>
<p>
First, they've got a custom CMS that they've licensed from a local design house but they don't have rights to the source code. So it took me forever to set everything up because I'd keep hitting little errors that stymied me because I couldn't go code spelunking. But I persevered (barely) and now I've got a local instance of the CMS running. (The custom CMS, it must be said, is overly complex and often inscrutable. Even the design house's lead developer had trouble explaining how it worked.)
</p>
<p>
The only way for me to develop what they need is to inject custom user controls into the page lifecycle. That's no big deal, just an annoyance. But if I want to see how something looks, I have to copy my DLL from one directory to another each and every time.
</p>
<p>
Second, the CMS is written and hosted in .NET 1.1. That means Visual Studio 2003 (retch) and trying to remember what subset of C# isn't available. A task which would be much simpler if I had a copy of my trusty ReSharper, which I don't. $149 is a lot of money to spend but I'm getting close to throwing in the towel and ponying it up. (I would never even think of pirating it.)
</p>
<p>
The final abomination is that the database is hosted on SQL Server 2000 and that means Enterprise Manager/Query Analyzer.  SQL Server Management Studio, part of SQL Server 2005, is so much nicer than that combo. Every time I fire up this suite of blast-from-the-past apps, I feel so dirty and ghetto. I'm hoping that someday soon they'll have the budget to allow me to convert over to an open-source CMS built in .NET 2.0.
</p>
<p>
The relationship with the non-profit and my belief in the rightness of its mission is what keeps me going on this when every fiber of my being says, "Go elsewhere, youngish man!" They got screwed with this custom CMS&#x2014;the peril of being non-technical&#x2014;and I wonder how the design firm sleeps at night seeing some of the atrocities I've come across. (If I ever feel spunky or get to migrate away from their CMS, I'll have some excellent horror stories to share. I should probably write them down somewhere for that eventuality.)
</p>
