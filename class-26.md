# Component Based UI

## Review, Research, and Discussion

**Name 5 Javascript UI Frameworks (other than React)**

_Angular, Vue, Ember, Svelte 3,and Backbone.js._

**What’s the difference between a framework and a library?**

_The technical difference between a framework and library lies in a term called inversion of control,When you use a library, you are in charge of the flow of the application. You are choosing when and where to call the library. When you use a framework, the framework is in charge of the flow. It provides some places for you to plug in your code, but it calls the code you plugged in as needed._

## Vocabulary Terms

**Rendering :** _Rendering is the creation of a visual representation - a picture or a movie - of data, such as a 3D model or a video composition._
**Templates :** _A template is a form, mold, or pattern used as a guide to making something_
**State :** _In information technology and computer science, a system is described as stateful if it is designed to remember preceding events or user interactions;[1] the remembered information is called the state of the system._

## Preparation Materials

_Component based UI systems like React, Angular, Vue, and the like all operate on similar architectural principles._

_Rather than view an application as an enormous interconnected codebase, the application is a composition of components that work together to make the application work._

_The secret sauce is how they work together._

_We use Classes and Functions to classify functionality._

_We require what we need._

_We render it where we want._

_we pay attention to state and react as it changes._

### React

_We will be using React in this course to learn these basic principles._

_As a component based system, React does an awful lot for us, principally, it gets out of the way and makes it EASY to implement your application the way you see it, using familiar tools._

### JSX

```
const element = <h1>Hello, world!</h1>;
```

This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.
