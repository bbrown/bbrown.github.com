---
layout: post
title: Service Hydra
date: '2006-03-16 00:51:00 -0700'
mt_id: 1095
blog_id: 1
post_id: 1095
basename: service-hydra
categories:
- net-development
---
<p>I recently had occasion to create a Windows service that was actually two Windows services within the same process. It was quite an ordeal because there is practically no documentation out there aside from the comment in the Main method of the service class automatically placed by VisualStudio .NET.</p>
<p>For posterity, here's what I learned:</p>
<ul>
<li>"Error 1083: The executable program that this service is configured to run in does not implement the service." This occurs when there's a mismatch between the ServiceName in the InitializeComponent method of the service (or wherever you've set such things) and the project installer. Both services need to match.</li>
<li>In the project installer, there should only be one ServiceProcessInstaller instantiated and one ServiceInstaller per service.</li>
<li>There should only be one Main method for the entire service and it doesn't appear to matter which service has it.</li>
<li>Each service should be defined as if it were an independent service. For all intents and purposes, it is. They will show up in the Service Manager as separate services and can be controlled independently.</li>
<li>I'm not particularly clear on the advantages or disadvantages of this approach. Design-wise, this method suited my needs.</li>
</ul>
<p>I hope this helps someone searching for this information.</p>
