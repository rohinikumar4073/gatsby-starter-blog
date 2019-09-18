---
title: DOJO nightmares
date: "2019-09-17"
description: "Nightmares caused by DOJO framework"
---

I was able to fix the issue mentioned on 16th dec. The issue was using a singleton for renderer and it keeps on adding the listener but it has never destroyed;
As DOJO uses AMD any module it is executed only once.

```
define([],function(){
    class A{

    }
    return new A()
})
```
The above code creates a singleton.