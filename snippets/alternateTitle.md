---
title: Alternate page title
tags: browser
expertise: beginner
firstSeen: 2022-05-25T22:16:38+0000
---

Sets a web page title to cycle between given strings at a specified time interval.

- Use `setInterval()` and `document.title` to animate a browser tab title.
- Set the `ms` variable to the number of milliseconds desired for the pause.


```js
const alternateTitle = (ms, titleA, titleB ) => {
  return setInterval(() => {
    (document.title !== titleB) ? document.title = titleB : document.title = titleA;
    }, ms);
};
```

```js
// Switches page title between a default value and 'Example Alert' every 1 second
const marquee = alternateTitle(1000, document.title, 'Example Alert') 
// Delete the SetInterval object to return to a static page title
clearInterval(marquee)
```
