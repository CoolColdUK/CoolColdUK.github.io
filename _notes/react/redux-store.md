---
tags: react,redux
---
Store is the object that brings them together. The store has the following responsibilities:

* Holds application state;
* Allows read access to state via getState();
* Allows state to be updated via dispatch(action);
* Registers listeners via subscribe(listener);
* Handles unregistering of listeners via the function returned by subscribe(listener).
