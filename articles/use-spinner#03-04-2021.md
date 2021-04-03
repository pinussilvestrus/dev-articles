---
title: use-spinner - Show loading spinners for your asynchronous calls
published: true
description: Add a simple loading spinner to your async JS calls - built for the browser.
tags: #showdev #javascript #webdev #programming
//cover_image: https://direct_url_to_image.jpg
---

Hello community :wave:

Sometimes calls can take longer, so showing a loading spinner becomes an option to fill the gap. I was tired of configuring such spinners times and times again.

Yesterday I built a tiny Javascript library called [`use-spinner`](https://github.com/pinussilvestrus/use-spinner) that simply wraps asynchronous calls into a new function adding a loading spinner to the DOM.

Simply install the module

```sh
$ npm install --save use-spinner
```

and embed it in your Node.js styled application.

```js
import useSpinner from 'use-spinner';

import 'use-spinner/assets/use-spinner.css';

const mySlowCall = async () => {
  return await fetch(/*...*/);
}

const spinned = useSpinner(mySlowCall);

await spinned();
```


![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bv6g2hpitdr8rhv43pw7.gif)

Of course, it is rather rudimentary right now and the spinner itself is hardly customizable. However, I like the easiness of integration to existing functions without much configuration.

Enjoy :heart:

{% github pinussilvestrus/use-spinner %}