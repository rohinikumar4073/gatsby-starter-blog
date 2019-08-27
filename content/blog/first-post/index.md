---
title: First post
date: "2019-08-19"
description: "100DAYSCSS expereince"
---

This is my first post.
I would like to start by sharing my experience working on 100DAYSCSS trend. The objective is to learn new CSS techniques by doing short CSS tasks given in [100DAYSCSS](https://100dayscss.com/).

Here is the [link](https://codepen.io/collection/nrGrOw/) to my collection of CSS works. I am currently at 43 days out of 100 days. 

I would like to explain **stroke-dasharray** and **stroke-dashoffset** in this first post. These can be given as tag attributes or CSS class properties on  SVG objects like circle, polyline or polygon.

The stroke-dasharray gives you how the dashes appear on the stroke of the SVG. 
For example stroke-dasharray : 4 1 2 3 means, there would dashes at 4 and 2 units and  blank spaces at 1 and 3.

The stoke-dashoffset gives you the offset of the dashes at the start.

With these two features we would be able to achieve cool effects of filling the stroke of the circle. 
1. **stoke-dashoffset** and **stroke-dasharray** equal to circumference of the circle
2. Using animation CSS reduce the **stoke-dashoffset** 
3. Keep **stoke-dasharray** value constant
```
circle {
        stroke:red;
        stroke-width:10;
        stoke-dashoffset:100;
        stroke-dasharray:100;
        animation:fill 2s;
}
@keyframes fill{
        0% {
            stroke-dashoffset:100;
            stroke-dasharray:100;  
        }
        100% {
            stroke-dashoffset:0;
            stroke-dasharray:100;
        }
}
```