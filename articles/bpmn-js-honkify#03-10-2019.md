---
title: Building a honkify extension for bpmn-js
published: true
description: bpmn-js extension which is inspired by honkify
tags: #webdev #bpmn #bpmn-io #javascript
---

Something for the fun department: Yesterday I found this amazing project, which replaces any link on a page with a duck "honk": [honkify.js](https://github.com/jlengstorf/honkify).  This inspired me to build a simple [bpmn-js](https://github.com/bpmn-io/bpmn-js) extension which adds this honk on several modeling operations, e.g. adding, moving or removing BPMN shapes from the canvas:

```js
/// Honk.js

import CommandInterceptor from 'diagram-js/lib/command/CommandInterceptor';

import inherits from 'inherits';

import showToast from 'show-toast';

export default function Honk(injector) {

  injector.invoke(CommandInterceptor, this);

  const audio = new Audio(
    'https://res.cloudinary.com/jlengstorf/video/upload/q_auto/v1569957993/honk-sound.mp3',
  );

  function _honk(context) {

    console.log('honk fired.', context);

    // honk
    audio.play();

    // show toast
    showToast({
      str: 'Honk 🦆🦆🦆!',
      time: 500,
      position: 'top'
    });
    return false;
  }

  this.execute([
    'shape.create',
    'shape.move',
    'shape.delete'
  ], _honk);
}

Honk.$inject = [
  'injector'
];

inherits(Honk, CommandInterceptor);
``` 

I put the results in a [small GitHub project](https://github.com/pinussilvestrus/bpmn-js-honkifay), which everyone can simply install via `npm` and directly integrate into their [bpmn-io](https://bpmn.io) application. 

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/t2y0ruenpelh3i2gee6b.gif)

This fun example showcases how easy it is to build extensions for the bpmn-io toolkit. Also, have a look at the [bpmn-js-nyan-cat](https://github.com/bpmn-io/bpmn-js-nyan) for another little example of how to bring joy in your modeling application.

Enjoy!