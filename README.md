**ImageApi.JS**<br>
A simple module to grab random images from a subreddit. Examples:<br><br>

[![npm](https://img.shields.io/npm/dt/imageapi.js.svg?style=for-the-badge)](https://npmjs.com/package/imageapi.js)

```js
;(async() => {
    const api = require('imageapi.js');
    let fetched = await api("subreddit"[, verbose is either true or false])
    console.log(fetched); // logs the image;
    let advanced = await api.advanced("subreddit"[, verbose is either true or false]);
    console.log(advanced); // { img: string, res: number, title: string, upvotes: number, author: string };
})();
```

I added in the following for a new update:

```js
api.fetched; // Returns an array with all images fetched.
```

I also added

```js
await api.stats(); // returns an object containing stats on imageapi.fionn.cc (async)
```

Along with

```js
api.clearFetched(); // Removes all elements in api.fetched
```

I hope this helps you!

**TYPESCRIPT!**

In version 1.1.0+, ImageAPI has now got built in typings, this is how you'd use the default function:

```ts
import ImageAPI from 'imageapi.js';
;(async() => {
    await ImageAPI('meme');
    //etc
})();
```
How you use .fetched, .advances, .stats etc
```ts
import * as ImageAPI from 'imageapi.js';
ImageAPI.fetched
```