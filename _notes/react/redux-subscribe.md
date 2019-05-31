---
tags: react,redux
---
The function in subscribe will be triggered whenever a change of state occured.

```javascript

const unsubscribe = store.subscribe(() => {
    console.log(store.getState());
});
```