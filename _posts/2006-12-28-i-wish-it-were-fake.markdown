---
layout: post
title: I Wish It Were Fake
date: '2006-12-28 09:33:00 -0700'
mt_id: 1176
blog_id: 1
post_id: 1176
basename: i-wish-it-were-fake
categories:
- programming
- net-development
- personal
---
<p>
If there is one thing I cannot stand at work <strong>it is wrestling with my tools</strong>. I've got two Web projects in Visual Studio 2003. I hate Web projects, hate 'em&#x2014;there is no reason that I've found that you cannot do a Web application using just a standard project and it makes life so much easier since Web projects are the devil.
</p>
<p>
Anyhow, I have to make this mission-critical change to one of the Web projects and neither one  will load automatically. Fine, I've danced this dance before about a month ago when suddenly Visual Studio refused to allow those Web projects into the solution. You just have to remove them and re-add them each time you open Visual Studio or change solutions. Man, after writing that, I can see how messed up my work life is&#x2014;constantly rerouting around lost settings, malfunctioning applications, and halfassery in order to get things done.
</p>
<p>
So I did that and one of the Web projects loaded. Well, it loaded on the second attempt to add it. Again, not an unusual thing as I also discovered that the first Web project added generally needs to be done again since the Web server takes too long and times out. At least, that's my presumption because it works the second time. (Insert existential scream here.) The second one, however, refuses to load, giving me a timeout every single time I try it.
</p>
<p>
Usually, I can just f'ing Google the error message and have a handful of things to try. Unfortunately, this seems to be a problem unique to me since I couldn't find a single instance of my particular error message. The help, unusually helpful on this topic, didn't even list my failure as one of the options in its lengthy catalog of possible messages and vague steps to resolve them.
</p>
<p>
I tried the usual panoply of magic actions that sometimes yield results: restart VS, restart Windows, go directly to the project instead of using the braindead Web project loader, create a new solution, and try again the next day hoping that last night's hell was just a bad dream. Nothing worked. Went to the IIS logs to see what sort of things Visual Studio was trying to do to load the sucker: lots of unfamiliar actions ("PROPFIND", never heard of it&#x2014;oh it's a WebDAV thing, interesting) and lots of 403s.
</p>
<p>
Ahh, the 403. Permissions. I know something about that. The permissions for both Web projects appeared to be the same, but let's just give those muthas full control. The panacea of frustrated users (and bane of administrators). Nothing. Machine.config: give the app SYSTEM access instead of ASPNET. NOTHING. NOOOOOOOOOOOOOOOOOOOOOOOOOTTTTTTTTTHHHHHHHING!
</p>
<p>
So three hours completely wasted while a mission-critical fix waits. I ended up editing the file in Notepad; now I just have to figure out how to <code>csc</code> a Web application. I hate wrestling with my tools.
</p>
<p>
[UPDATE: Great news! I got the Web project loaded &#x2026; <em>but the source control bindings were lost</em>. The words "Pyrrhic victory" spring to mind. Visual Studio and source control binding problems are a separate level of hell unto themselves. Bleh.]
</p>
<p>
[UPDATE 2: In a dramatic turn of events, it bound. I hit the "Bind" button in the Change Source Control dialog and it came back in a few seconds. I was dumbfounded. It's never worked that well without manual diddling about in the VSS-VS project files. Finally.]
</p>
