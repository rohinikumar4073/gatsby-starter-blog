---
title: Learnings
date: "2020-02-19"
description: "Learnings "
---

# Redirecting images using meta tags
This meta tag in the head will automatically refresh page in 5 sec. The number in content indicates how long it will wait before redirecting.
```
<meta http-equiv="refresh" content="5;url=http://example.com/" />

```
# Animating Hide and show pages as elements added and removed by a box
It is difficult to animate as we are removing children and adding children. As elements are getting added and removed dynamically the height of the parent changes so we could add transition animation property to the parent height.The parent height has to be set by caluculating based on children.
https://codesandbox.io/s/eager-field-vj9xo


