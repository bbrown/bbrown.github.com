---
layout: post
title: The Command Prompt
date: '2006-06-16 12:10:00 -0700'
mt_id: 1127
blog_id: 1
post_id: 1127
basename: the-command-prompt
categories:
- programming
- future-reference
---
<p>This is going to seem like yesterday's news to my fellow Mac OS X and Unix readers, but I just got something working today that is pretty impressive in the Windows command prompt.</p>
<p>I love this <a href="http://www.interlog.com/~tcharron/grep.html">Windows version of "grep"</a>&#x2014;I install it on every server and desktop I interact with. It's super fast, very similar to the Unix version, and I've never had a single problem with it.</p>
<p>I was trying to use its output as input for another command. This is called "command redirection" in the Windows world and "piping" everywhere else. Sadly, the documentation on the Web about this feature of Windows is sparse. I can see why: Windows executes both commands simultaneously and if the receiving command wasn't designed to wait for standard input then it'll just error out. Like the "del" command, for example. Non-Windows users are welcome to snigger quietly now.</p>
<p>Then I found <a href="http://www.windowsitpro.com/Article/ArticleID/39958/39958.html">this article</a>. This isn't piping per se, but the idea is the same. Take the output of one command and use it in another. Once I had that, it was a simple <code>for /f "tokens=*" %a in ('grep -l stuffIwantDeleted *.FOO') do del %a</code>. Worked like a dream!
</p>
