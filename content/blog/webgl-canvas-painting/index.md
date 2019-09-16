---
title: WebGL Canvas drawing layers issue
date: "2019-09-14"
description: "Drawing overlapping ARCS"
---

WEBGL has   a JavaScript API that will draw on canvas in 3D world. It uses GPU of the native machine. Rendering is an energy consuming process and using the native GPU might help in being efficient.

Recently a collegue has an interesting issue in the space.The issue is very tedious to debug as the code is in WEBGL JavaScript API. It has lot of new API's. 

The issue is as follows. The code prints three arcs. The first arc spans three rows. The second has two rows and the third has only one row. Each Arc has different color and three are coming out of one vertex. But each of them have different depths.Ideal way should be each layer having its own colors but as we draw there is a gradeint on each layer. 

I believe in WEBGL as we color the vertex and use the shaders to draw, the vertex color is propagated and it is forming gradients. But as they are using different depths for each layer and each layer has different color the gradient should n't have formed.

I have tried instead of drawing all the layers at once , drawing each layer might fix this issue and it has worked. The issue might have resolved now but I am not sure really happening.
