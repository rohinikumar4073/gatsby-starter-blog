---
title: Auto expand feature in tree JavaScript
date: "2019-09-09"
description: "Implementing auto expand of a node on hover during a drag operation of a node"
---

Today my colleague was implementing an interesting feature. This is a tree widget feature where a node is dragged on to the other node. The collapsed node would autoexpand if the drag hover exceeds a certain period of time.

The asynchronous operations are tricky. Here there are multiple hover events are emitted on hovering on a node. 

The psuedo code solution for this problem

1. On hover set a Timeout and save the timeout variable and the domNode in outerscope.
2. If there are mutiple hovers on the same node then the timeout should not be set again
3. If there is a hover on differnt node then we have to clear the timeout and again start the timeout.

I am trying to find any other way we could fix this problem.
In CSS there is animation we could control to apply after certain period of time, we could use this solve this issue.
