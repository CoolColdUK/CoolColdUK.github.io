---
tags: redux, react
---
Functions that generate action objects. Benefit includes
* reduce chances of typos in action string
* if typo occur, it will give out an error as it is an actual function
* can make use of intellisense

```javascript
const incrementCount = ({ incrementBy = 1 } = {}) => ({
    type: 'INCREMENT',
    incrementBy
});
```
if object is passed, it will destructure to variable ```incrementBy```.
If no object passed, it will have default empty object. IncrementBy will be defaulted to 1
incrementBy is the same name as variable so it can be used to create object directly.