---
title: Creating the unknown - What and what not to build in efficient prototypes
published: false
description: Lessons Learned in the DMN Innovation Process
cover_image: https://dev-to-uploads.s3.amazonaws.com/i/14846d35rp5w2m4mky76.jpg
tags: #webdev #ux #prototyping
---

In the last couple of quarters, I did a lot of work in improving the overall modeling experience for the [dmn-js toolkit](https://bpmn.io/toolkit/dmn-js/). We decided on an approach that would rather go with building prototypes instead of real features. 

This allowed us experimenting, elaborating, and iterating a lot with the tremendous amount of decision modeling ideas we had at the beginning. Along this road, I learned a lot, so I decided to write down my thoughts about the overall process and what, from my experience, makes a prototype _efficient_.

### Background: Agile Prototyping

Generally saying we moved along an _Agile Prototyping_ process while creating our prototypes. I won't go too much into detail about that topic, [this blog post](https://www.atlassian.com/blog/agile/agile-design-prototype) explains it quite good.

What we keen to do all the time was to improve our prototypes with each iteration. Beginning with the most important or most obvious feature, we tried to add more and more to the actual demo, until we were sure the original feature fits our users needs. This included a couple of user tests to verify our assumptions, or to improve the demo with our findings. 

Starting with a demo instead of a real implementation gave us enough flexibility to try out multiple things for a specific problem. We were simply not coupled to internal conventions `dmn-js` would have given us.

Once we have to tackle a bigger problem, about which we do not know much yet, it makes total sense to start with that approach. Take the time to experiment and learn about the problem before you actually start solving it. The next chapters should explain about some learning I've made during this time. 

### Know the use case

Before creating a demo showcase, it's necessary to know a particular use case you want to test. Not every scenario is suitable for creating a prototype for it. Most bug fixes and feature requests are quite trivial in the end. Once you don't know how the feature would look in the end, maybe because there wasn't built something like that before or there are a bunch of possible solutions, it's a perfect starting point to think about creating a prototype.

There will be a dedicated chapter for that point, but: Don't start with too many scenarios. Try to think about the **basic user story** you want to solve. Is there a particular problem your users face multiple times? Is there a specific request your application should serve. Before you begin, try to create a basic user journey. After you created that one, try to think about variable routes the journey could take. Once you know the basic scenario, it will be easier to define a specific interaction for the prototype.

I can recommend [this blog post](https://uxplanet.org/a-beginners-guide-to-user-journey-mapping-bd914f4c517c) for first guidance on how to create pleasant user journeys.

### It's about Innovation + Inspiration

It's okay not always to create entirely new functionality. Although the problem would be huge and uncertain in its possible solutions, most stuff was already solved out there. Inspiration is not cheating. The users are often used in certain ways of solving different problems. 

That's why it makes total sense to take solutions from other applications and check whether you can bring it inside your prototype. In some cases, there might be standards that give a basic guideline on how to solve problems. Doing such a **pre-research** often helped me before getting started with the ideation step.

![](https://dev-to-uploads.s3.amazonaws.com/i/jw8kjwow18au3dp87q6s.png)

Also, you have to deal that your prototype solutions follow the design guidelines of your application. It depends on the use case, but creating a sidebar control panel when you only use popup modals in the current state might not be a good idea.

This should not hold from bringing the innovation into your work. Creating prototypes is the perfect time to go crazy. Whenever it's suitable, think about unusual solutions. Whether they are ideal in the end, you'll find it out in the user testing.

### Start with a pen

Don't start coding! As it is best practice to not fixing the bug right away, but first [shaping the problem](https://basecamp.com/shapeup), you should do the same with your prototype. Depending on how big the problem is, start with  **sketches** or low-fidelity prototypes. So, pen and paper!

![](https://dev-to-uploads.s3.amazonaws.com/i/14846d35rp5w2m4mky76.jpg)

Try to take some time and illustrate as many solutions as possible. Also, try not to doing it alone. Spreading and sharing ideas helps to create synergies. As one of the dozen possible methods to drive the sketching and ideation phase, I can recommend to try out [Design Studio](https://www.edenspiekermann.com/insights/working-with-design-studios/).

Starting with a sketch helps to express and change ideas more frequently. Since you're just at the beginning, don't be coupled to technical solutions. It also enabled us to have first user test scenarios with some sketches itself to get the earliest feedback as possible. 

After several iterations and once we were confident we found the right solution, we went into creating paper prototypes or quickly starting with the actual demo, depending on your needs. Sketches have a lack of illustrating interactions. Combining sketches to a paper prototype enables the chance to bring the idea to life.

![](https://dev-to-uploads.s3.amazonaws.com/i/hdmg5httc0k4a3dc206o.png)

Btw., for creating sketches, I can really recommend trying out [Excalidraw](https://excalidraw.com/). Of course, starting with a pen as a first step is indispensable. But then converting more shaped ideas into a virtual sketch helps to illustrate some aspects more deeply.

### It's not a feature branch

I mentioned it a couple of times before, but do **not stuck on your codebase**. Try to create demos from scratch. Why? Because oftentimes, your codebase gives you restrictions on what and how to build stuff.

Prototyping is a phase of the development cycle where you want to try out crazy ideas. Creating your demo on a blank HTML page helps to create whatever you want, without dealing with technical limitations. Do not overengineer stuff. You know the use case of the demo, so build the demo application right for that purpose. There will be time to think about the final implementation later on.

I lately wrote a [blog article about creating demos with Svelte](https://dev.to/pinussilvestrus/creating-demos-with-svelte-2gem).

### Keep it simple

That one should be clear now. Once you know the user story of your prototype, try to keep it in that scope. Furthermore, don't intend to reinvent the wheel. You need an autocomplete input? Try to integrate a working library for that. Modals, icons, drag and drop functionality? Try not to build it yourself. Of course, there will be cases where you have to create something from scratch again so that these components fit your needs. Most of the cases, it's okay to re-use certain stuff.

![](https://dev-to-uploads.s3.amazonaws.com/i/u4p0julbmmkyhfm5jqu8.gif)

Additionally, do not implement all edge cases inside your prototype. **Focus on the problem your demo should solve**. Do not get stuck on extra cases that might affect you in the future. The primary purpose should be to verify your idea with the user. Make sure you give your testing person a scenario to click through. 

That's the most crucial stuff which should work smoothly. Any extra stuff is a bonus. Often the case, crazy other functionality might also distract the testing user from the main focus, which would have a negative effect as well.

### Build fast, fail faster

Since you want to be agile in your prototyping phase, plan multiple iterations. You won't find the best solution at the beginning, that won't work. Take user testing sessions to verify your ideas. Does the user like it? Keep it. It was confusing, or the user had problems to solve your problem? Think about alternatives and improve the demo. 

Step by step, you will find the best or at least a very good solution that fits your needs. I often heard that prototyping might be a waste of time, especially when you throw it away at the end. It's okay to throw stuff away. The main goal of this phase should be to **make learnings**. Get to know the problem, try out different solutions, and learn.

### Think about variations

When you're doing the user testings, try to think about variations of your solutions. Because then, you will have a side-by-side comparison inside the demo. The user faces multiple ways of solving the same problem and can directly express what he likes the most. Often, in the end, the solution will be a mixture.

When creating variants, make sure they **only differ in specific aspects**. The rest should be exactly designed the same. Why? If one option might have, for example, another color, other dimensions, or simply nice looking icons, the user might feel one solution to be the best for the wrong reason. You want to know which way of solving is the best, interactionwise. So the user should not be distracted from surrounding things.

For us, it was also a good idea to implement variant toggles inside the demo application. It gave us the flexibility to quickly jump from one variant to another, e.g., via clicking a badge on the right upper corner or via keyboard shortcut. Also, we sometimes had remote user tests, so the user had to control the application entirely itself. Having such a simple variant toggle implemented was the easiest way to test all variants after each other without wasting time between them.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/uwmx2xnitwyv5tgcacgi.gif)

### Keep the best

The first goal should be to make learning, as I described before. After you did some user tests, went over several iterations, you might have a solution in which you're confident it will solve your problem in the final application. Will you implement all features of your demo? **No, of course, not**. 

After the concept phase, it's time to reflect. Pick the best aspects and think about how to bring them into your real application. Scope your findings and start with the low-hanging fruits. As the prototyping phase was a time of iterations, the implementation phase should follow the same guideline. 

### Summary

To summarize, I made the following lessons learned while creating the DMN prototypes:

* Know the use case
* It's about Innovation + Inspiration
* Start with a pen
* It's not a feature branch
* Keep it simple
* Build fast, fail faster
* Think about variations
* Keep the best

You might not implement all stuff from your demo, although the user liked them a lot, due to technical or time limitations. That's okay, and you won't throw them away, keep them for coming releases. The prototyping phase shows you many aspects you didn't think about before. If there's one suitable solution, in the end, it was highly worth it.

For me, it was the first time dealing with prototyping and creating demos in a more extended period. It came out the field of Usability Engineering as something very valuable during the development cycle, especially when the problems got bigger with a higher amount of uncertainty.

I tried to link some other interesting blog posts inside my writings. If you have any other thoughts, opinions, or questions, feel free to reach out!

