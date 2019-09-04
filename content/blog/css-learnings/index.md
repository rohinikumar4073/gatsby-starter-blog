---
title: CSS learnings
date: "2019-09-04"
description: "Transform Style, Perspective & background-size"
---
## Transform Style
1. transform-style property works on the parent

``
transform-style:preserve-3d;
``
2. transform-style on the parent helped to make the translate3d work in the z-direction for the child

``
transform:translate3d(0px,0px,-0px);
``

## Perspective
1. Perspective also works on the parent and children    
2. This is the distance from the z-plane

``
transform:perspective(60px);
``
## Background size
1. Background size can accept cover which makes the background image to cover the full view.

``
background-size:cover;
``