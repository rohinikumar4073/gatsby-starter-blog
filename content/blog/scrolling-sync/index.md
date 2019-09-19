---
title: Scrolling sync
date: "2019-09-20"
description: "Synchronizing scrolling"
---

This was a hard problem to solve. The problem is syncing the scroll between various containers. Browsers emit scroll event after every scroll. The Scroll happen if  the *scrollTop* or *scrollLeft* is set  or any external event caused the scroll to be changed. Triggering the scroll using an simulate event seems to be not possible.

During scroll synchronisation this leads to infintie loop. Let us take two containers.

container 1  scrolled -> Scroll Event on container 1 -> Sync Container 2 -> container 2  scrolled-> Sync Container 2 -> container 1  scrolled 
This leads to an infinte loop. 

(syncscroll)[https://github.com/asvd/syncscroll] has helped us to solve this issue. As we look into the code this was solved by breaking the loop by using a global variable.

Sets Globar varible <- container 1  scrolled -> Scroll container 1 -> Sync Container 2 ->  Container 2 scroll -> Sync container 1 (checks for global varible and breaks the loop)  