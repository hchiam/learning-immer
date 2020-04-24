# Learning Immer

Just one of the things I'm learning. <https://github.com/hchiam/learning>

<https://immerjs.github.io/immer/docs/introduction>

```js
import produce from "immer";

const baseState = [
  {
    todo: "Learn typescript",
    done: true,
  },
  {
    todo: "Try immer",
    done: false,
  },
];

// use immer's produce function:
const nextState = produce(baseState, (draftState) => {
  // update immutable state as if you're directly mutating state:
  draftState.push({ todo: "Tweet about it" });
  draftState[1].done = true;
});
```
