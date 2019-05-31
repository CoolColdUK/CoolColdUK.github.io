---
tags: react,redux
---

create store is needed to start a store object
@param state current state, or default state if not passed
@param action action passed by dispatch function

>createStore(reducer, [preloadedState], [enhancer])

```javascript
import { createStore } from 'redux';

const store = createStore((state = { count: 0 }, action) => {
    console.log(action.type);
});
```

above code will created a default state in the first parameter, and create an action in the second parameter. The store can be accessed by any part of the program.

>The state should never be changed directly. It should be returned.
