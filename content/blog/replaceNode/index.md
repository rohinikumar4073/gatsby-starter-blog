---
title: Replace Node & DIJIT Destroy
date: "2019-10-29"
description: "Replace node in DOM"
---

## Replace NODE JavaScript
Today I came across this API during the code review
``
domNode.replaceChild(newNode,oldNode);
``

This API seemed interesting to detach and attach the dom nodes at a certain position.
https://codepen.io/rohinikumar4073/pen/mddMgmO

## DIJIT Destroy
DIJIT is DOJO Widget system to develop widgets declaratively. It has a mixin named Destroyable. This helps to destroy the widget. The DIJIT widget has **own** method. The Classes that inherit the destoryable class implement this function and place things that are going to be destroyed inside the function.
### Tear Down Life cycle Of Dijit

    destroyRecursive
        destroyDescendants
        destroy
            uninitialize
            destroyRendering