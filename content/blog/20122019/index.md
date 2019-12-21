---
title: "ADDING ONE AT TIME OR ALL AT ONCE"
date: "2019-12-20"
description: "ADDING ONE AT TIME OR ALL AT ONCE"
---
Our team works on web widgets. Today I got a query from downstream team about a performance issue they are seeing. 
This is regarding a Tristate checkbox tree widget  . In this widget ticking a checkbox would check all the nodes in the tree. There can  also be a mixed state on the parent nodes which indciates there are mixed state  of nodes xin the child nodes.
## Issue
The issue is when they are trying to add around 1000 nodes one by one and they are seeing performance issues. 
## Root Cause
One of the reasons it is taking a long time is for each node added to a parent, the parent state is caluculated. The state of the parent node doesn't have a state on its own and it is caluculated from all the children state. 
## Solution
One of the way we can solve this is by adding all nodes at once so there is no need to caluculate for every addition and node state is calucated.

```
// There is an API already by our team
dataStore.replaceAll(data);

```
This took considerably less time.

