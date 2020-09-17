---
title:  jQuery prev and jQuery prevAll API
date: "2020-09-10"
description: "Learning"
---
##jQuery Prev
The prev API gives the previous sibling of the current node which is adjacent to the node.
It also accepts the selector as a parameter. If the selector and the previous node matched it returns the node.
The catch is I assumed the prev selects any element that matches the selector which on the top of the tree structore from the current node, but it works only on siblings.

##jQuery prevAll
The prevAll API gives all the previous elements of the current node which are siblings to the current node.
It also accepts the selector as param, if the selector and pervious sibling nodes in the tree mathces it gives them in the reverse order.

The document API which is equivalent previousSibling