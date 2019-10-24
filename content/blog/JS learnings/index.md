---
title: JS Learnings and SVG ViewBOX
date: "2019-10-23"
description: "Recent learnings"
---

## document.documentElement

This returns the HTML DOM. Useful in cases where body and html dimensitions differ.

## SVG ViewBox

I wasted lot of time on a bug misinterpretting what ViewBox means.ViewBox is dimensions for SVG which translatex the pixels to SVG world.
ViewBox has for attributes. 
1. minX  Starting value of X
2. minY  Start  ing value of Y
3. Width
4. Height

```
For example width = 30px height = 20px   and the ViewBOX is '0 10 30 20' then the dimensions is as below.
0,10         30,10
--------------
|            |    |        
|            |    |
|            |    30px   
|            |    |         
|            |    |         
--------------
0,30         30,30

------ 20px ----
```

## Flex box pseduo selectors

If the DOM element with the display flex and it has pseduo after and before they also behave as flex box children.

https://codepen.io/rohinikumar4073/pen/JjjNorW