---
title: Writing Utility function
date: "2019-12-15"
description: "Recent learnings"
---

Recently I faced a kind of challenge while writing some code in javascript. I was repeating lot of *if* conditions in my code. I am not happy about it. The code basically checks for an variable exists or not and assigns to another variable. This is to transform an object to another object.

```
    
if(s.b){
    a.b = s.b;
}
if(s.c){
    a.c = s.c;
}
if(s.d){
    a.d=s.d;
}
```
After a lot of thought I came up with a basic way of handling this situation and make my code little better. I abstracted this functionality to a method and called this on the variables with key and values.

```
function assignVariable(obj,key,value){
    if(val){
        obj[key]=val; 
    }
}
let {b,c,d} = s;
assignVariable(a,'b',b);
assignVariable(a,'c',c);
assignVariable(a,'d',d);

```