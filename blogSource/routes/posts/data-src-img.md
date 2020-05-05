---
template: post.html
title: data-src property in <img> tag
date: 2020-05-05
---
### Whyyy???
To do fancy stuffs like offloading image load to web worker

`<img>` tag block application load. The browser will download all the images first before rendering page.

The browser start downloading immediately when encountering `<img>` tag with a `src` attribute. People use custom property, usually `data-src` to break this behaviour. Then define the desired behaviour. 

This usually done to lazyload images.