---
layout: post
title: Let's See the Polished Draft Now
date: '2008-06-10 08:09:10 -0700'
mt_id: 1294
blog_id: 1
post_id: 1294
basename: lets-see-the-polished-draft-now
categories:
- mac-os-x
- high-geekery
---
<p>
After reading <a href="http://twitter.com/Ihnatko/statuses/830746587">Andy Ihnatko's tweet</a> about Apple's announced solution to the lack of background processing on the iPhone, I realized that I had been taken in by Steve Job's famous <acronym title="Realty-Distortion Field">RDF</acronym>. It sounded good to me while I was listening to it—I mean, except for the September release. But I didn't think much about how little the single-source notifications addressed the problem it ostensibly solved until I read <a href="http://whydoeseverythingsuck.com/2008/06/iphone-background-processing-not-fixed.html">Hank Williams' excellent analysis</a>.
</p>
<p>
Basically, the single-source notification is good for handling incoming alerts that need to be displayed to the user in any application but doesn't address the other two compelling cases for background processing: a) notifications like an alarm clock or countdown timer and b) broadcast messaging for status updates or location notification. Updating a badge with a new count of incoming messages is nice but it really limits the sort of application possible using the new features and API.
</p>
<p>
Can you imagine the extra work a developer of a countdown timer app would have to do to tell the user that the timer has reached zero? When the countdown timer app is exited due to a call or another reason and the timer hadn't elapsed, he would have to send a final message out to his server on the Internet indicating the remaining time and the iPhone in use. Then the server would notify Apple when the timer elapsed and Apple would alert the user. But the application would spawn this process even if the user intended to quit the timer app or even if there was two seconds left. Further, it seems like Apple's server would queue update requests so it's entirely possible that the user would be alerted long after the timer had actually elapsed.
</p>
<p>
For status broadcasting, there's just not going to be a way to handle it in the single-source scenario as it appears to be a one-way process. Sites like <a href="http://brightkite.com/">Brightkite</a> or <a href="http://fireeagle.yahoo.net/">Fire Eagle</a> couldn't get the particular iPhone to respond to a pull request because I'm sure that Apple would not allow a notification to quit the running application to open a different one. That would make for a jarring user experience and I just don't see Apple going that route.
</p>
<p>
Obviously, details about this September service are sketchy at this point so all of these considerations could prove moot when it is released. But Apple had better address them because no countdown timer app maker would provide a server to accommodate Apple's unwillingness to allow background processing and location-based social networking seems to be a compelling use of the new GPS capability.
</p>
