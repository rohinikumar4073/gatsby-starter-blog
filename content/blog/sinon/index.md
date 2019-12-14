---
title: Sinon
date: "2019-12-07"
description: "Sinon for Architecure Firday"
---

Sinon JS provides spies, stubs and mocks for JavaScript. This works with any unit testing framework.

Spies look out things like number of times the function has been called, with what kind of arguments it has been called and so on.

```javascript
var spy = sinon.spy()
spy(1)
spy(50)
console.log(spy.callCount)
console.log(spy.withArgs(1).callCount)
```

Stubs are canned answers. It has all the methods of the spies. This is used to replace a function in an object also.

```
var stub = sinon.stub().returns(50);
console.log(stub(1));
console.log(stub(50));
let obj = {
    meth : function(){
        console.log('from oring')
    }
}
function fn(params) {
        console.log('from dup')
}
sinon.stub(obj, 'meth').callsFake(fn)
obj.meth();

```
Mocks are also predetermined answers. The mock has its expectations upfront. Mock.verify can be called to verify if the expectations are accurate.

```
var mock = sinon.mock(obj);
mock.expects("method").once().throws();

```