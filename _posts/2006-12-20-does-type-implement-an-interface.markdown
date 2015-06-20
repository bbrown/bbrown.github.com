---
layout: post
title: Does Type Implement an Interface?
date: '2006-12-20 12:07:00 -0700'
mt_id: 1172
blog_id: 1
post_id: 1172
basename: does-type-implement-an-interface
categories:
- future-reference
- net-development
---
<p>
I've wasted far too much time on this issue, so I'll make an entry for future frustrated Google searchers. You're welcome.
</p>
<p>
If you need to see if a particular Type object implements a particular interface, it's clear that the <a href="http://msdn2.microsoft.com/en-us/system.type.isassignablefrom.aspx">method <code>IsAssignableFrom</code></a> is the proper choice. But the damn thing wouldn't work. <code>is</code> certainly what I was looking for. Then I found <a href="http://www.hanselman.com/blog/CommentView.aspx?guid=9ee062df-c3c6-4121-90d4-304a9cad3de3">Scott Hanselman's entry on the subject</a> and it became obvious that I was reversing the members.
</p>
<code>
<pre>
Assembly library = Assembly.LoadFrom(pathToLibrary);
Type[] allTypes = library.GetTypes();
foreach (Type type in allTypes)
{
if (typeof(IInterfaceToImplement).IsAssignableFrom(type))
{
doYourThing(type);
}
}
</pre>
</code>
<p>
Previously, I was doing <code>if (type.IsAssignableFrom(typeof(IInterfaceToImplement))</code> and it just wasn't doing it's thing.
</p>
