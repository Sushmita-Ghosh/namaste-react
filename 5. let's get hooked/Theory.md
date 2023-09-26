### What are React Hooks?

A hook is a normal JS func that is given by React- these are prebuilt - comes with utilies

- Whenever state variable updates react re-renders the component.

- The logic of updating the UI is known as re-rendering, and this is where react is great, This is what makes react fast, it handles DOM updates reallly well.

### What is reconciliation?

### What is React Fibre?

The reconciliation algorithm is also known as react fibre in react-16. It is new way of finding the differences and updating the DOm
[REACT FIBRE REPO](https://github.com/acdlite/react-fiber-architecture)

### What is virtual DOM?

VD is representation of an actual DOM. It is actually an object
VD as a concept existed a long before REact came into existence but REact was only built using the same concept.

### What is diff algorithm?

React creates a Virtual DOm from actual dom
Diff Algo basically finds out the differences between two virtual doms. Once it finds out the difference
then the differences will be applied to actual DOM
React is not touching the actual DOm a lot which is why it is fast

### Why is REact fast?

React is fast as it does efficent DOM manipulation.

### UseState

- Usestate basically returns an array - what we do is array destructring

```jsx
const arr = useState({ name: "bhupinder" });

const [name, setName] = arr;

// The above two lines is same as below - it is array destructring

const [name, setName] = useState({ name: "bhupinder" });
```
