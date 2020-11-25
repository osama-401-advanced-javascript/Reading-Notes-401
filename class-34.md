## Review, Research, and Discussion

**Why is the Context API useful?**

Well it is very useful when we need to define a global state that we can use in each components without the need to have a relation between those components

**Can a component outside of a provider get its context?**

Yes, by importing the context to that component

**What are some common use cases for using the Context API?**

For Authentication, to make sure that the user is registered or not each time the user is trying to do something in the website .

Describe “Context Hell”

## Vocabulary Terms

**global state :** It is a state that can be accessed/updated from any component in the application

**global context :** A set of methods/function or states that can be accessed from any component in the application without the need for the relation between these components

**provider :** Its a React context that will provide some methods/states to the whole application as global

**consumer :** It is a React component that is using the the context provider.

## <Login /> and <Auth />

The <Auth /> component helps make authentication and role-based authorization easy.

Based on your permissions and login status, it either gives you access to a component or JSX or hides it.

// The div only shows if you are logged in

```
<Auth>

<div />
</Auth>

// The div only shows if you are logged in AND have read permissions
<Auth capability="read">

<div />
</Auth>
```
