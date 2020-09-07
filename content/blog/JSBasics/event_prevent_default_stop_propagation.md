---
title:  Event Prevent Default
date: "2020-09-07"
description: "This answers some questions in JavaScript"
---

## event.preventDefault

In the events like form button or links, there are certain default actions are performed.
This would stop the browser from performing any default behaviours

```
<form onsubmit="submitform()" action='/b'>
  <input>
  <button >Submit</button>
</form>
function submitform () {
  event.preventDefault()
}

```

## event.stopPropagation

This would stop the events from propagating to the parent


## event.stomImmediatePropogation
This would stop the events from propagating to the same level and also to the parent.
```
document.querySelector(".child-b").addEventListener("click", function () {
  console.log('child b 1')
  event.stopPropagation();
  event.stopImmediatePropagation();
});
document.querySelector(".child-b").addEventListener("click", function () {
  console.log('child b 2')
});
document.querySelector(".parent").addEventListener("click", function () {
  console.log("from parent");
});


```