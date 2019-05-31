---
tags: react,redux
---
Reducers specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.

This is the function passed to the createStore function
>type Reducer<S, A> = (state: S, action: A) => S

>Reducer are [pure function](../programming/pure-function.html)

```javascript
function todoApp(state = initialState, action) {
  switch (action.type) {
    case SET_VISIBILITY_FILTER:
      return Object.assign({}, state, {
        visibilityFilter: action.filter
      })
    default:
      return state
  }
}
```

> Note: state do not mutate