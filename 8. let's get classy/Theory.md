### CLass Based Components: (CC)

Class based components at the end of the day are normal js classes

- render: renders a piece of JSX

### Why do we write super(props)?

- A child class constructor cannot make use of this until super() has been called; also, ES2015 class constructors have to call super() if they are subclasses.

- When you want to access this.props in constructor.

- passing or not passing props to super has no effect on later uses of this.props outside constructor. That is render, shouldComponentUpdate, or event handlers always have access to it.

[REF]("https://stackoverflow.com/questions/30571875/whats-the-difference-between-super-and-superprops-in-react-when-using-e")

### Constructor:

- best place to recieve props and create state variables
- In CC, the state is a big object that contains all our states- no need to define the state differently each time for new state like we do in FC

### Never update state variables directly:

- means this.state.count = this.state.count + 1 --> this is wrong
- we can do -->

```javascript
this.setState({
  count: this.state.count + 1,
});
```

- whenever the state updates react rerenders the component again - so it will show new value
- if there are 4 -5 states & we are only updating two - react will not touch the other states

### LifeCycle Methods:

- Whenever a react encounters a CC , an instance of the class is called and whenever an instance of the class
  is called then constructor is called
- then render
- once component is successfully renderred componentDidMount is called

### Why are the api calls made inside ComponentDidMount?

So, how react works is react first renders the components --> then makes api call --> then fills the componnet with the data. Hence api call will be made inside CDM then component will again get rendered.

- Idea is to render the component as fast as possible then make the api call.

### REact has 2 phases - Render phase and Commit phase -

- Render phase is fast as it deals with rendering of the components - no side effects [constructor/render]
- Commit phase is slow - side effect (componentDidMount & Dom updation)

If react finds more than 1 child - react will batch the render phase together and then execute the commit phase for all. This is an optimization part- Means the render- constructor will be execute first for parent and the children - after that all the componnetdidMount will be called.

### Unmounting Phase - componentwillUnmount

- return from useEffect
- when used - if we have a useInterval say in useEffect to do something - we need to clearthe interval otherwise even if we switch routes our interval will keep on running and cause a overhead to our application.

### Why we can't have the callback function of useEffect async?

- componentDidMount api call we can make it async to use await but cant do for useEffect- React screams an warning at us.
- You cannot directly make the callback function supplied to the useEffect hook async because:

  - async functions implicitly return a promise, and;
  - useEffect expects its callback to either return nothing or a clean-up function.
