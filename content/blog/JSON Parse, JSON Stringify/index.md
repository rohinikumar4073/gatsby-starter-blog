---
title: JSON Parse, JSON Stringify
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