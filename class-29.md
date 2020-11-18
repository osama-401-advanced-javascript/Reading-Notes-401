# Routing

## Review, Research, and Discussion

- **Do child components have direct access to props/state from the parent?**
  _the child have an acsess through th props_

- **When a component “wraps” another component, how does the child component’s output get rendered?**

```
<Main>
  <Content />
</Main>
```

- **Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?**
  yes

* **What trick can a parent use to share all props with it’s children?**
  _Make the parent warp the child before execution_

## Vocabulary Terms

- **props.children** _array of objects that represent all the children as markup that the parent has ._

- **composition** _react method allow to wrap markup inside the component as children ._

## Preparation Materials

## Routing

- _Using `react-router`, you can easily toggle the visibility of componenets (or even pages) based on the URL/Route that the user engages with._

- import {Route} from 'react-router-dom';

- To use Browser Router properly, you eliminate your use of <a> tags and instead use its built-in <Link> component.

```
<Link to="/">Home</Link>
<Link to="/stuff">Stuff</Link>
```

- In practice, then, use the router componenet to look at either / or /stuff and based on that, displaying either the Home or the List component, like this:

```
 <Route exact path="/" component={Home} />
 <Route exact path="/stuff" render={() => <List>{items}</List>} />
```
