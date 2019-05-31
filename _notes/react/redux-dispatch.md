---
tags: react,redux
---
Dispatch means perform an action

> type BaseDispatch = (a: Action) => Action

```javascript
store.dispatch(
    {
        type: 'INCREMENT',
        incrementBy: 5
    }
);
```

The parameter is an object, which at least contains a field called 'type'.