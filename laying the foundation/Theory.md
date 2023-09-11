- React createElement => React ELement(which is an Object) => HTMLElement(rendered as in root.render)

### What is JSX?

- JSX is a javascript syntax which is easier to create REact elements.
- React can be built without JSX as well, JSX makes developers life easy hence we easy
- It is not HTML inside Javascript. It is HTML -like syntax

- Javascript(ES6 or other version) is understood by JS Emgines but JSX is not (so how is it being converted to JS engine understandable - by Parcel )

- Parcel transpiles JSX code before it reaches JS engines (but Parcel is not doing this job )
- Transpilation is handled by Babel package (JSX => React.createElement)

### WHat are React Functional Components?

- Normal JS Funcs which return a react element/ JSX code

### What is component composition?

- Componnet inside component - we are composing two componnets into one another

```jsx
const Title = () => <h1>Title Component</h1>;

const HeadingComponent = () => (
  <div>
    <Title /> // This can also be witten as {Title()} -> as Functional
    components are normal JS functions
    <h1> Heading Componnet </h1>
  </div>
);

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(<HeadingComponent />);
```

-JSX takes care of Cross Site Scripting acttacks for us . It will sanitise out data before unning.
