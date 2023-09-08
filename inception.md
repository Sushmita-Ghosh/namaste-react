### What is cdn?

CDN stands for content delivery network. It is a place where content is hosted and if we use the same link
in our code, we will pull the resources from there.

### What is crossorigin in cdn links ?

### React DOM

This is the object that we need to modify the dom.

- There are different type of places where react is used not only in browsers, like react native so there are two files react & react dom.

### React.createElement

createElement takes in 3 attributes:

1. tag
2. tag attributes - props
3. what we want inside thes tag - children

```javascript
React.createElement("h1", { id: "heading" }, "Hello from React");
```

React.createElement returns an object - Symbol - it is a react element - it is an object

- The <b>render</b> method is responsible for converting it to an html dom elemnet & put up in the root

### What will happen if there is already something in the div with id root?

The code gets replaces when it encounters render method. WHateever lies inside the root will get replaced
