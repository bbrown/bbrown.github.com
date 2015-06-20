---
layout: post
title: Unrewarded Persistence
date: '2007-10-09 02:30:00 -0700'
mt_id: 1242
blog_id: 1
post_id: 1242
basename: unrewarded-persistence
categories:
- net-development
---
<p>
Boy, do I really want to love <a href="http://www.codeproject.com/aspnet/PersistAttribute.asp">this technique</a>.
I mean, who wouldn't prefer this:
</p>
<p>
<code>
[PersistField(Location = PersistLocation.Session)]<br />
public bool IsLoggedIn;
</code>
</p>
<p>
Over this:
</p>
<p>
<code><pre>
public bool IsLoggedIn
{
get
{
return Convert.ToBoolean(Session["IsLoggedIn"]);
}
set
{
Session["IsLoggedIn"] = value;
}
}
</pre></code>
</p>
<p>
It's so elegant and so concise. But it operates through reflection and
reflection has a bad rap for being hoggy. Can you imagine checking every
property for the attribute on load and then checking to see if they've
changed at on unload? Talk about a tax on resources.
</p>
<p>
This beautiful snippet trades readability for performance and I think the
bargain isn't worth it. The time it takes to write out the getters and
setters of a property is a one-time deal. The decoration method outlined
above makes the code easier to read and easier to describe, but at the
expense of perennial runtime delays.
</p>
<p>
It's just not worth it.
</p>
