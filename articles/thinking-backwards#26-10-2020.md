---
title: "Thinking Backward - or: searching for the Big Why"
published: false
description: How thinking and working backward gets your product-work focused.
tags: #productivity #product #agile 
//cover_image: https://direct_url_to_image.jpg
---

Where to start? Every product work begins with this question; let it be ideating a completely new product idea, creating a simple feature enhancement, or fixing a crucial bug.

I once wrote [another blog post](https://dev.to/pinussilvestrus/creating-the-unknown-what-and-what-not-to-build-in-efficient-prototypes-467p) about prototyping and how to use it to tackle uncertain problems. 

At [Camunda](http://camunda.com/) we follow the strategy to keep our work focused. One thing at a time, but doing this one right. That's great, but how do you know what this *one thing* is?

One principle my team more or less actively used in the past is to *work backward*. This could sound like guessing the right solution, right? Let me explain.

### Working Backwards © Amazon

The idea of working backward is not new, [Amazon "introduced" it a while ago](https://www.inc.com/justin-bariso/amazon-uses-a-secret-process-for-launching-new-ideas-and-it-can-transform-way-you-work.html). At the very beginning of developing new products, the product manager, or even better the team, writes an internal press release about the finished product. Before creating a single user story, without writing a single line of code.

The press release should be customer focussed, stating why current solutions are failing and why users will be amazed by the new product. Having this as a "solution sketch" they start iterating, keep on improving it. The key here: "Iterating on a press release is a lot less expensive than iterating on the product itself (and quicker!)" (Ian McAllister). 

I never wrote such a press release as the working backward method requires. What's important to me here are the principles that are behind. That's why I'd rather call it *Thinking Backwards*. It does not start with a press release, an MVP, a mockup, or a prototype. It starts with thinking.

### It's all about shaping

[Basecamp did tremendous work in the past](https://basecamp.com/shapeup) to define what shaping of tasks means for successful product development. You could argue it's not feasible for any organization to do those 6 weeks of focused working sprints where the team is absolutely autonomous without any surrounding noise.

![shape up](https://dev-to-uploads.s3.amazonaws.com/i/mr2mj82ajv38n3fc7zs5.png)
<figcaption>Shape up phases by Basecamp, source: https://basecamp.com/shapeup/4.1-appendix-02</figcaption>

What's even more important is the *shaping* part at the beginning. Avoiding circles in the development phase is a key part of our work at Camunda. 

In the end, it's a matter of avoiding waste. Taking more time to *really understand*  the problem and identify the core need will produce waste as well. That's okay if you compare the potential waste and problems of redefining requirements and refactoring huge parts of your implementation at the very end of the development lifecycle.

The Shape Up "manifesto" from Basecamp itself has this nice sentence: "If we don't make trade-offs upfront by shaping, the universe will force us to make trade-offs later in a mad rush".

Of course, there will be cases where you feel spending more and more time shaping a topic will cause more effort than needed. What's really important in this phase is to gather *learnings* and create *focus* on the most relevant aspects. 

Afterward, it will be much easier to simply get the stuff done, without getting lost in circles. Build the one thing which matters and do it right. Which does not mean that circles in the implementation phase are bad. But that's another topic.

### Begin with the problem - jump back if necessary

Shaping comes along with thinking about the problem in a deeper manner. I tend to start with the following question: what is the main problem we want to tackle and why will users be *amazed* by it? That's not easy for sure and depends on a lot of prerequisites and hypotheses you still have to find out.

![double diamond](https://dev-to-uploads.s3.amazonaws.com/i/jdr9qbp4tj9e1vqkcbdg.jpeg)
<figcaption>The Double Diamond of creating solutions, source: https://www.smashingmagazine.com/2020/05/research-study-double-diamond-model</figcaption>

With this saying, the double diamond is worth to be mentioned. Despite [this model might have some weaknesses](https://uxdesign.cc/why-the-double-diamond-isnt-enough-adaa48a8aec1), it shows a very relevant aspect: all the research, all the shaping you do in regards to find a solution, it all aims to find the main problem and to deliver a focus. 

The problem: sometimes it feels like a waterfall. Defining the problem, then defining the requirements, then creating the solution. That's indeed not ideal. The solution space is always re-opening the space of the problem. Therefore it's recommended to take steps back, evaluate the problem, and re-shape it. You may name those problems to be "wicked", Horst Rittel did [a lot of ground keeping work](https://nnsi.northwestern.edu/wicked-problems-what-are-they-and-why-are-they-of-interest-to-nnsi-researchers/) in this regard.

By the way: if you also love those diagrams about the double diamond and design thinking, give this website a try: https://designfuckingthinking.tumblr.com/.

### Find the Big Why

"Users have to be amazed by the product", that's the spirit of Amazon's working backward method. That's far from being easy. This requires a lot of research to get the real *needs* of a user. That's not a high-level exercise, it really goes into the psychology of users while working with our products.

Thinking backward about the product which needs to be build creates a new perspective. We ask: what makes our users happy? Is there a particular need our product needs to serve?

I don't want to go too much into detail. What's important is that we can directly influence the way users adopt new products and features by building them in the way they deal with basic psychological needs. 

Don't understand me wrong, it's absolutely not about creating an interface which "looks nice" and the user enjoys from a visual perspective. It's about functionality. 

That's the "Big Why". [Hassenzahl and Diefenbach](http://www.experienceandinteraction.com/tools) did a lot of research on this topic.

### It does not have to be a press release

It can be anything that is not a technical prototype nor a design sketch. To give some inspirations 

- write a letter from a user
- write a product review from a user
- create a promotion video
- create a user onboarding
- create a getting started guide

![letter from a user](https://dev-to-uploads.s3.amazonaws.com/i/dttsozvr4bb32ppw5nro.png)
<figcaption>An imaginary letter from a user I recently created in a UX Thinking training (German). The project scope was an application for shared traveling.</figcaption>

At Camunda we recently did the last thing. The project was about creating an embeddable library that our customers can easily integrate into their existing Javascript applications.

It helped a lot to get an understanding of what the end-users will see at the very first. What would they expect? What are the actual steps they need to do to integrate our library? We took this sketch of a getting started guide, reflect & iterate on it with customers, and came closer to real requirements, step by step.

This perspective helped on focussing on the most important aspects: What should the user be able to achieve and how can we provide it in the easiest way. Remember: the user has to be amazed.

### Summary

...
