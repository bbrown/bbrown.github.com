---
layout: post
title: WebException and the HttpWebResponse
date: '2009-02-20 21:29:00 -0700'
mt_id: 1406
blog_id: 1
post_id: 1406
basename: webexception-and-the-httpwebresponse
categories:
- web-tech
- blogging-world
- high-geekery
---
<p>The following code is used to make a request and get the results:</p><code>HttpWebRequest req = (HttpWebRequest)WebRequest.Create("http://bbrown.info/");<br />HttpWebResponse resp = (HttpWebResponse)req.GetResponse();<br />StreamReader reader = new StreamReader(resp.GetResponseStream());<br />string contents = reader.ReadToEnd();<br />resp.Close();</code><p><code>contents</code> will contain the HTML of this blog <em>if the server gives a <code>200 OK</code> response</em>. Anything else will throw a <code>WebException</code>. You can wrap the snippet above in a try-catch to handle a non-<code>200</code>, but the exception is thrown in the <code>GetResponse</code> call so you get <em>nothing</em> from the actual response. <code>404</code>? May as well be a <code>500</code>.</p><p>Today I discovered that the <code>WebException</code> itself has two properties: <code>Response</code> and <code>Status</code>. This <code>Response</code> is the same as the <code>resp</code> above so you can extract out the server response in the catch.</p><p>This whole behavior of <code>HttpWebRequest</code> is counterintuitive in the sense that a non-<code>200</code> is not an exceptional circumstance; I would have expected the response to be accessible and the status code to be populated.</p>
