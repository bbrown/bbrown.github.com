---
layout: post
title: G5 Benchmarks from NASA
date: '2003-07-04 02:06:46 -0700'
mt_id: 312
blog_id: 1
post_id: 312
basename: g5-benchmarks-from-nasa
categories:
- high-geekery
---
<br />An engineer at <acronym title="National Aeronautics and Space Administration">NASA</acronym> has put up a <a href="http://members.cox.net/craig.hunter/g5/">page</a> describing the tests he's conducted using a dual-2.0 GHz G5, a dual-1.0 GHz G4, a dual-1.25 GHz G4, a 2.0 GHz P4, and a 2.66 GHz P4. He ran benchmarks using the same NASA software on all five machines. The software was optimized for the AltiVec-engine of the G4, but not further optimized for the G5's 64-bitness.<br /><br />To be fair, he even hobbled the dualies by running them the software on one <acronym title="Central Processing Unit">CPU</acronym> only. The results show that the G5 is quite competitive with the P4s ("within 1 MFLOP of the 2.66 GHz P4", "32% faster than the 2 GHz P4"), lays waste to the G4s ("97% faster than the 1.25 GHz G4", "142% faster than the 1 GHz G4"), and offers much better MFLOPs per MHz ratios (0.127 MFLOPS/MHz versus 0.096 MFLOPS/MHz for the P4s).<br /><br />There's been a lot of crowing lately about Apple cooking the benchmarks. That may be&#x2014;though I don't buy it entirely&#x2014;but they also suggested that benchmarks aren't how one should compare computers. Instead they recommend&#x2014;and I totally agree&#x2014;that real-world applications that exist on both platforms should be used.<br /><br />Here we have some evidence that high-end applications do quite well with the new G5s. In fact, when the second processor was brought online, MFLOPS soared up to 498 versus the 255 for the P4 in the scalar test (which doesn't let the AltiVec-engine offer its advantages) and 5177 MFLOPS in the vector test (which the P4 can't participate in because it doesn't do vector computation like the G4 and G5 do). It achieved all this while maintaining a MFLOPS/MHz ratio of 0.126 in scalar and 1.29 in vector&#x2014;suggesting that dual processors roughly equal two independent processors.<br /><br /><br />
