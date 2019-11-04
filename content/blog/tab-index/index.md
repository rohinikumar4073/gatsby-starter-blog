---
title: TAB INDEX
date: "2019-11-05"
description: "TAB index 0 ,-1 and 1"
---

Pressing keyboard Tab helps to navigate across different focusable elements*(input)* in the browser window. 

Specifying **tabIndex = 0** on the non-focusable elements like div makes them focusable. This element would also be included in the navigation order of the page.

The **tabIndex = -1** won't make the node include in the navigation order but this could be focused on click or programticaly like below.

``
element.focus();
``

The **tabIndex = 1** didn't work for me at all.

https://codepen.io/rohinikumar4073/pen/gOOvewv