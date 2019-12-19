---
title: A Lightweight React Library for creating clickable Prototypes
published: true
description: Lightweight React Library for creating clickable Prototypes
tags: #prototyping #react #sketch #ux 
---

As a little Holiday project, and as a follow-up of the DMN Innovation Week we had at [Camunda](https://camunda.com), I created [a small React components library](https://github.com/pinussilvestrus/clickable-prototype) to quickly create clickable prototypes. 

Inside Innovation Week, we created multiple small prototypes to test various ideas on how to improve the DMN experience in [bpmn-io](https://bpmn.io). Inside that, I used `jquery` to create a click-prototype and use it inside user tests. The results can be seen in this [GitHub repository](https://github.com/pinussilvestrus/drd-relation-prototype).

Yes, jquery is not the *best* solution to save the application state, like to save the actually visible view. Therefore I wanted to have a simple library that managed the interaction between different screens/views and where I only have to declare the click points which should direct to the next view. 

I've chosen `React` and created the [`clickable-prototype`](https://github.com/pinussilvestrus/clickable-prototype) project. It offers different components to declare your clickable prototype. A simple React Application using that would like that

```jsx
import React, { Component } from 'react'

import { View, HitBox, ViewContainer } from 'clickable-prototype'

import view1 from './views/view1.png'
import view2 from './views/view2.png'

export default class App extends Component {
  render () {
    return (
      <div>
        <h1><span>clickable-prototype</span> Demo</h1>
        <ViewContainer defaultView='view1' className='container'>
          <View
            key='view1'
            className='custom-view'
            screen={view1}
            width='1220px'
            height='630px'>
            <HitBox
              position={{y: 380, x: 477, width: 280, height: 60}}
              to='view2' />
          </View>
          <View
            key='view2'
            className='custom-view'
            screen={view2}
            width='1220px'
            height='630px'>
            <HitBox
              position={{y: 490, x: 477, width: 280, height: 60}}
              to='view1' />
          </View>
        </ViewContainer>
      </div>
    )
  }
}

```

This will result in the following prototype

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/wvom18t0sfuibjolkqyu.gif)

It's a very early stage of the library but it helps me a lot to quickly create clickable prototypes without any extra fancy stuff as you'd have in applications like [InVision](https://www.invisionapp.com/).

I would really appreciate if you give it a try and give some feedback!