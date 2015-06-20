---
layout: post
title: Rick, Rick, He's Our Man
date: '2008-04-01 00:50:02 -0700'
mt_id: 1269
blog_id: 1
post_id: 1269
basename: rick-rick-hes-our-man
categories:
- web-tech
- humor
---
<p>
Over at <a href="http://www.foundontheweb.org/">Found on the Web</a>, I've made my first April Fool's joke. As you <a href="/2008/03/04/my-contribution.aspx">might expect</a>, it's Rick-Roll related.
</p>
<p>
Here's the Javascript I used:
</p>
<pre><code>
&lt;script type="text/javascript" language="javascript"&gt;
var links = document.getElementsByTagName("a");
for (var i=0; i &lt; links.length; i++)
{
links[i].onclick = function()
{
location.href=&quot;http://www.youtube.com/watch?v=oHg5SJYRHA0&quot;;return false;
};
}
&lt;/script&gt;
</code></pre>
<p>
It gets every hyperlink on the page, loops over them, and adds an <code>onclick</code> event handler that performs the redirect.
</p>
