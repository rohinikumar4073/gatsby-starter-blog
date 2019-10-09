---
title: Drag And Drop A11y
date: "2019-10-09"
description: "Drag And Drop A11y"
---

Though I am working on the drag and drop for long I have never looked into acheiving Drag and Drop using keyboard to support a11y.

https://dev.opera.com/articles/introduction-to-wai-aria/ 
This link by Gez Lemon helped me to understand a11y in general. 
 The summary of the article is the the ARIA attributes basics. The custom components(widgets) are developed using JavaScript. These are not accesible by default as they are not native Desktop compoenents. We can make these widgets accesible by providing aria attributes. This attributes helps the assitive technologies to understand the widgets.

 https://dev.opera.com/articles/accessible-drag-and-drop/
This link also by Gez Lemon helped me to understand a11y in drag and drop. 
 Drag and Drop ally has two aria attributes. 

## aria-grabbed
  This attibute is set to true, false or undefined
  1. If this attribute is set to *true* then the drag and drop has started.
  2. If this attribute is set to *false* then the item can be dragged
  3. If this attribute is set to *undefined* then the item cannot be dragged

## aria-dropeffect
This is a list of items that are set on the drop targets. The values are *copy*, *move*, *reference*,*execute*, *popup*  and *none*.  These is set on the object that the item has to be dropped.
