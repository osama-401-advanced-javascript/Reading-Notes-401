## Custom Hooks

**First released in October of 2018, the React hook APIs provide an alternative to writing class-based components, and offer an alternative approach to state management and lifecycle methods. Hooks bring to functional components the things we once were only able to do with classes, like being able to work with React local state, effects and context through useState, useEffect and useContext.**

### Five Important Rules for Hooks

- Never call Hooks from inside a loop, condition or nested function
- Hooks should sit at the top-level of your component
- Only call Hooks from React functional components
- Never call a Hook from a regular function
- Hooks can call other Hooks

### React Hooks with Async-Await

**We cannot use 'async' keyword with 'useEffect' callback method. It will result in race conditions.**

### useReducer

`const [state, dispatch] = useReducer(reducer, initialArg, init);`

- An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

- useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
