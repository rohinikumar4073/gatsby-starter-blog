---
title: SetTimeout and calling the function earlier
date: "2019-09-26"
description: "SetTimeout and calling the function earlier"
---

# Problem
A method has to execute after a sec, but if there is an user action it has to be executed before that timer gets completed.

# Solution 1
The solution just clears the timeout and calls the function on its own. 
```
 let timeout= setTimeout(callback,1000);

 on('interrput',function(){
     clearTimeout(timer);
     callback();
 })

```

# Solution 2

An elegant way would be using [Timeout library](https://github.com/rommelsantor/Timeout) 

```
Timeout.set('time1',callback,1000);
on('interrupt',function() {
    if(Timeout.exists('time1'){
        Timeout.clear('time1');
        callback();
    }
});

```