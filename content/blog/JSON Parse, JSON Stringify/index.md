---
title: JSON Parse, JSON Stringify & Flex box margins
date: "2019-10-31"
description: "Recent learnings"
---

# JSON Stringify

JSON.Stringify converts a JSON Object to String. In case of Set, Map it is converted to arrays. It is undefined for Symbol.

JSON.Stringify accepts second parameter as a function called replace which helps to replace any value.

JSON.stringify accepts third parameter for indentation,
https://jsbin.com/yotoyiy/1/edit?html,css,js,console

# JSON Parse

JSON.parse converts String to JSON. 

It  has second parameter reviver. 

Both functions are working for the conditional statements. Its not working if we return directly some vlaue.

https://jsbin.com/yotoyiy/2/edit?html,css,js,console

# Flex box Margin right and  left

Today I have noticed in a flex negative values of margins will increase the width and the positove values will reduce the width of the flex box.
https://codepen.io/rohinikumar4073/pen/qBBVrVG

# rgba

CSS RGBA is very useful to give the opacity only to the background and not the children.