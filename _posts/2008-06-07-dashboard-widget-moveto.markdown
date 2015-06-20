---
layout: post
title: Dashboard Widget moveTo
date: '2008-06-07 04:50:58 -0700'
mt_id: 1292
blog_id: 1
post_id: 1292
basename: dashboard-widget-moveto
categories:
- mac-os-x
---
<p>
If you find yourself whipping up a widget in Dashcode and circumstances have moved that widget (during the running and testing) off the screen so that you've essentially lost it, you'll try everything to get it back. <code>window.moveTo</code> doesn't work. There is no <code>widget.moveTo</code>. And manually setting <code>window.screenTop</code> to <code>0</code> has no effect. So you google and google and google, but there's seemingly no query that you can construct to get an answer. I guess you're never going to see your little widget again.
</p>
<p>
But don't despair, friend! Just use the undocumented method <code>widget.resizeAndMoveTo(<span title="x coordinate: 0 means left side of screen. You can use window.screenLeft to find its current position.">x</span>, <span title="y coordinate: 0 means top of screen. You can use window.screenTop to find its current position.">y</span>, <span title="The new width of the widget. You can use window.innerWidth to get the current width.">width</span>, <span title="The new height of the widget. You can use window.innerHeight to get the current height.">height</span>)</code> in your <code>show</code> method and you'll have your widget right where you want it, safe and sound.
</p>
