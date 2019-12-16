---
title: ClientWidth OffsetWidth ScrollWidth, Usability and a11y 
date: "2019-12-17"
description: "Learnings"
---

## ClientWidth

ClientWidth is the width of the DOM excluding the scrollbar includes padding.

## Offset Width

Offset width is the width of the DOM including scroll bar, padding and border and nargins. 

If the scroll bar is not present OffsetWidth will be equal to ClientWidth.

## ScrollWidth

ScrollWidth is the width of the domNode eve the scrollbar is not present.

## Code to Detect whether hover to scrollbar
```
function isHoverOnScrollbar(e){
    return e.target.clientWidth <= e.offsetX || e.target.clientHeight<= e.offsetX;
}
```
https://codepen.io/rohinikumar4073/pen/XWJNMLr

## A11y

A11y and Usability are different things. 
Usability in simple terms how the system can be really usable to people.
A11y on other hand is the system accesible for different people.
This gives a different perspective of UX. 


