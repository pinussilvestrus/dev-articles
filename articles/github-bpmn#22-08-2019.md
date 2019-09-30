---
title: render-bpmn: Upload and Display BPMN | CMMN | DMN Diagrams on Github
published: true
description: Applications Collection: Render BPMN, CMMN and DMN files on GitHub
tags: javascript, productivity, github, bpmn
---

The [2019 Camunda Summer Hackdays](https://twitter.com/Camunda/status/1164197803792490502) was a good place to work on long-time planned projects which I had no time for the last months. After three days we built a good working prototype on how to render BPMN diagrams on GitHub. [Checkout](https://github.com/pinussilvestrus/github-bpmn) and leave some feedback or a star out there ⭐️.

### General Problem

It's currently hard to display BPMN files on GitHub. In the case of images, the application offers post-processing of the uploaded files in order to quickly display them. Unfortunately, this does not work for process diagrams. This kind of diagrams can be really helpful to outline feature requirements or bug root analysis. Right now, it requires to open these BPMN files in an external tool, as [bpmn.io](https://bpmn.io), to properly display them _or_ to convert the files to images.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/2vntycntkyyjiazxb45r.png)

### Hacking Prototypes

In the 2019 Camunda Hackdays we wanted to create several prototypes in order to automatically render BPMN files in GitHub repositories. In the [resulted repository](https://github.com/pinussilvestrus/github-bpmn) we provide these solutions. It solves the problem in two ways:

__Automatically render BPMN files in Issues and Pull Requests__

The self-hosted [probot](https://github.com/probot/probot) application offers an auto-rendering of uploaded BPMN files via bpmn.io. 

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/t42rjzlna8a4lb96ddtu.gif)

__Automatically render BPMN, CMMN and DMN diagrams in repository file tree via hover__

You can easily include the resulted userscript via Tampermonkey or use the adapted Chrome extension.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/fm1696p32yu2q0if807a.gif)

### Conclusion

The resulting project offers an easy way to quickly display your beloved BPMN, CMMN or DMN files in your GitHub repository. We [plan to increase the feature set](https://github.com/pinussilvestrus/github-bpmn/issues) soon, as long we find time for that. Feel free to try out the solutions, we'd love to hear some feedback ❤️ and receive some 🌟 on GitHub.

