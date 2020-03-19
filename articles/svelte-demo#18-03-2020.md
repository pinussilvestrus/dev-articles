---
title: Creating Demos with Svelte
published: true
description: How I used Svelte for quickly creating Demos - Lessons Learned
tags: #webdev #ux #prototyping #svelte
---

**Note**: The Content was previously created inside [these slides](https://speakerdeck.com/pinussilvestrus/what-i-learned-from-using-svelte-for-the-demos).

We're currently creating a lot of demos and prototypes to improve the overall DMN modeling experience inside our [bpmn.io](https://bpmn.io/) toolkit. After designing the first demos with [jQuery](https://jquery.com/), because of having the ability to create UI stuff quickly, and experiencing some silly things related to reactivity and state management, I wanted to give [Svelte](https://svelte.dev/) the first try.

I heard about it a couple of times before, and the possibilities and vision behind it sound quite pleasant to me. I can recommend [this article](https://tsh.io/blog/svelte-framework/) to get a first glance about it.

![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/0b2cp158wvm0eao8vp3f.png)

So I went to create the next DMN demo with Svelte and get away from jQuery. The general feeling was excellent. In comparison to the last demos, the speed of creating view switching and simple interactions was halved in working time, at least.

That's why I decided to take some time and to reflect on it. The result was a quick lightning talk, which I discussed with my team. Next, I also want to share the main thoughts about it in this article.

### The Reactivity is 🔥

To compare, in the jQuery demos, it took a lot of boilerplate code to input something like reactivity into my application. 

Svelte is designed for exactly that use case. As an example, binding variables to a component template makes it way easier to react to changes in the state and switch to different views.

```html
<script>
    export let view;
    export let activeView;
</script>

<div
    class="wrapper"
    style="display: {view === activeView ? 'block' : 'none'}">
        {#if view === activeView}
            <slot/>
        {/if}
</div>
``` 

Furthermore, it allows me to react to user selections, for example, when the user changes the hit policy inside a DMN decision table quickly.

```html
<script>
    export let tableData = {};

    const HIT_POLICIES = [ /* ... */ ];

    $: explanation =
        find(
            HIT_POLICIES, 
            hp => hp.name === tableData.hitPolicy
        ).explanation;

    function changeHitPolicy(event) {
        const {
            target: { value }
        } = event;

        tableData.hitPolicy = value;
    }
</script>

<select on:change={changeHitPolicy}>
    {#each HIT_POLICIES as { name }}
        <option selected={name === tableData.hitPolicy}>{name}</option>
    {/each}
</select>
<p class="hp-explanation">{explanation}</p>
```

Imagine doing that with jQuery, it would take me some actions to rerender the explanation `p` node. Svelte, by design, is doing that for you.

### Component Templating

When creating my jQuery demos, I also tend to develop modules for different UI components. But even here, the boilerplate code to render this stuff was just pain.

Creating Svelte components is more comfortable than that

```html
<script>
    import Table from '../../../decision-table-layout/src/components/Table.svelte';
    import ArrowExpandSvg from '../../resources/arrow-expand.svg';

    import './NavigationTable.scss';

    const noop = () => {};

    export let onViewSwitch = noop;
    export let tableData;
</script>

<div class="navigation-table">
    <div class="buttons">
        <span class="arrow-expand btn btn-sticky" on:click={() => onViewSwitch('split-screen')}>
            {@html ArrowExpandSvg}
        </span>
        <button class="edit-drd btn" on:click={() => onViewSwitch('drd')}>
            Edit DRD
        </button>
    </div>
    <Table { tableData } />
</div>
```

It also allowed me to do particular re-use components, like the `Table` component, in other parts very smoothly. 

### Global State

Managing state can also be rough, and you tend to use specific state management libraries for that, like `Redux` in React. I was not forced to do something like that in my demo, but it was nice to get the overall data from one entry point and re-use that in all of my components.

So, whenever something of my table data changes, the different parts of my UI would be re-rendered due to those changes. There is no virtual DOM included, which makes it a bit faster. Svelte [itself explained briefly](https://svelte.dev/blog/virtual-dom-is-pure-overhead), why this approach solves some problems.

```html
<script>
    import data from '../resources/data.js';
    let currentTable = data['Decision_03absfl'];
    let view = 'drd';
</script>

<Wrapper view="drd" activeView={view}>
    <DRD decision={currentTable.id} />
</Wrapper>

<Wrapper view="split-screen" activeView={view}>
    <SplitScreen tableData={currentTable} />
</Wrapper>
```

### Summary

Honestly saying, I just started to use Svelte for my demo applications, and there are lots of more aspects to learn. The reason I did not switch to React, which I used a lot of times before, was simply that I wanted to give Svelte a chance. 

The general expression was very good. The development speed and experience was unexpectedly good. To be clear, it just *felt* very good to create this demo.

In comparison to jQuery, it makes things way easier, like reactivity and state management. I can recommend to try it out.
