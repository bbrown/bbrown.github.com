---
layout: post
title: A Hard Decision
date: '2008-09-26 23:39:28 -0700'
mt_id: 1363
blog_id: 1
post_id: 1363
basename: a-hard-decision
categories:
- programming
- net-development
- high-geekery
---
<p>
I've been a consumer of the <a href="http://www.codeplex.com/FacebookNET/">Facebook.NET</a> framework for a few months now as I've developed several Facebook applications in ASP.NET. I chose that framework instead of the <a href="http://www.codeplex.com/FacebookToolkit">official Microsoft one</a> because it seemed more logical and straightforward.
</p>
<p>
Honestly, I'm not at all certain why I originally chose one over the other. I read all of the blog commentary about each, I looked over the source, and I checked out the sample applications included. Facebook.NET struck me as elegantly designed, well conceived, and actively developed. Sure, Microsoft had commissioned and paid for the development and maintenance of the Facebook Developer Toolkit, which meant it was more likely to be around in the future. This possible objection was easily dismissed since Facebook.NET was open source and could be extended privately as long as need be.
</p>
<p>
What I couldn't have foreseen were sweeping changes by Facebook to the underlying API within six months and a complete abandonment of the open-source project by its sole maintainer. Facebook has made a lot of mistakes in handling the transition but there's precious little that I, as a third-party application developer, can do about that. So my sole responsibility is to keep up with updates to the framework and alter my code to accommodate the new (or changed) functionality.
</p>
<p>
Faced with a framework that isn't getting updates, the responsibility expands considerably. One must either abandon the abandoned framework to search for greener pastures or one must take up the mantle of leadership by forking the project. Neither is a path to be chosen lightly for each entails considerable pain.
</p>
<p>
The choice was made easier for me by the fact that the Facebook Developer Toolkit was just as inactive at the time. I tried corresponding with the Facebook.NET maintainer and even succeeded a couple times: I would much rather have been a developer on a project than the man responsible. In the end, it became clear that the maintainer had moved on to other projects and that I was going to have to fork.
</p>
<p>
The result is <a href="http://www.codeplex.com/fbnet/">fb.net</a>. I largely brought it up to parity with the API changes in a span of two days but then I got distracted by work, family, and other projects myself. As it stands, there's just a little more to go and then I can make a release candidate.
</p>
<p>
My only hope is that I can get this framework ready for a full release and then start looking to build a community that can assist in its maintenance. The Facebook.NET maintainer got it off to a good start; now it's my turn to finish the job.
</p>
