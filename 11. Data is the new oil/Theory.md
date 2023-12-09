### What is HOC in react?

HOC are functions which take in a component and return a component. It takes in an existing component , tweaks/enhances it a little and returns the same component back.

`Why do we use it?`

- reusability
- predictable - HOC are pure functions - the enhanced components are never changed directly

`Example`
In swiggy.com , there are some promoted restaurants - so we have a restaurant card - we can just add the promoted label to the cards that want it. So we can develop a HOC which will take our exiting restaurant card as a input and return the card with label.

### Lifting State Up:

There might be a use case - wherein keeping the state at the children level is not solving the problem at hand then we lift state up to the parent and pass the props to children.

`Example`

In the food app, in accordian section when one category is expanded the other should close - if we keep showitems in the child we will not be able to achieve this as each category has its own state- but if we lift the state up to parent - then all children will have common state and we can make all categories as closed when one is expanded.

### Controlled vs Uncontrolled

- Controlled Components can controll the state of child - stateless - no state of its own, they are controlled by parent components through props.
- Uncontrolled Components are those which are are those who have the control over state - if the component has its own state and,

### Props Drilling:

When the application is huge - components are nested - passing data in huge applications becomes a challenge - and react is one-way data flow.

`Example:`
RestaurantMenu -> RestaurantCategory -> ItemList
Suppose if we want to pass the a data from RestaurantMenu -> ItemList we need to always pass the props to RestaurantCategory - not directly . We will have to access the intermidiate parents.
Suppose our react app has 7 layers of nesting - we will still have to pass the props to all the componnets even if they do not use it .

### Context:

We can use something known as the context - which is kind of a global place to store all our states - accessible to all our components - Solves props drilling.

`Example:`

- LoggedIn User Info
- Theme

`Steps:`

1. Create a context - using createContext

```javascript
import { createContext } from "react";

const UserContext = createContext({
  loggedInUser: "Default User",
});

export default UserContext;
```

2. Context Provider - to update the context value anywhere in you app - Wrap you root component with UserContext.Provider

```jsx
<UserContext.Provider value={{loggedInUser: userName}}>
    <App>
</UserCOntext.Provider>
```

3. Use the context - useContext

```javascript
import { useContext } from "react";
const user = useContext(UserContext);
```

- If class based components we can use .Consumer - takes in a callback

```jsx
<UserContext.Consumer>
    {({user}) => <h1>{user}</h1>}
</UserCOntext.Consumer>
```

4. Contexts Provider can be nested , only the components inside the provider will have access to the state.
