### Single Responsibility Principal:

This states that any module (say a js function) should be responsible for one and only one actor(job).

According to that principal , each of the components should have a single responsibility.

##### Advantages:

- If we make our code more modular- writing test cases for our app becomes easier. - so it becomes <b>TESTABLE</b>
- It is easy to maintain modular code- easy to catch bugs - <b>MAINTAINABLE</b>
- It is easy to resuse the components - <b>REUSABILITY</b>

### Custom Hooks:

A hook is just a utility function.

Why we need Custom Hooks?
It helps us optimise our code - Suppose we have a RestaurantMenu component - which fetches data for displaying restaurant menus & also displays the same - So we can optimise the fetching of the data by writing a custom hook - as RestaurantMenu should only be concerned with displaying the menus. While it is not mandatory, it is a good practice.

###### 🔥 Good Convention:

Always create different files for diffrent hooks.

##### 🔥 Steps to writing custom hooks:

- Finalise the contract ( input & output)

##### 🔥 Example of custom hooks:

We can build a custom hook to show online status of the user . We can use the online event to do the same
[Window-online event](https://developer.mozilla.org/en-US/docs/Web/API/Window/online_event)

### How to simulate a offline experience using browser instead of turning off internet connection:

Inpect --> Network Tab --> Throttling (select Offline from dropdown)

### Is it mandatory to use the work "use" infornt of hooks or why do we write our componnets with first letter in caps in React?

- It is not a strict rule but react does recommend it- reason being - some projects might have linters setup which might throw an error if these
  are not followed.

- Easier for various developers to understand code better - when collaborating across a project.

### Parcel:

Parcel will bundle our code and just give one JS file with the code.
For large scale application - this posses as an issue - because js single bundle huge size will result in low performance - load time will be high.

To optimse this we can break our app bundle into smaller js bundle files for the components

This is known as code-splitting / chunking / dynamic import / lazy loading /dynamic bundling
(Break your app into smaller logical chunks.)

### How to make smaller bundles & when to make smaller bundles?

We can do logical seperation of bundles - means bundles should have enough code for a feature

- We can use React.lazy --> it takes in a callback and we have pass the path to import() return --> it is not similar to the import we write wile importing componnets it is a function

### "Error: Your component suspended while responding to a synchronous input"

When we lazy load our components we face this error - as since react is very fast - it tries to load the components before the code comes to the browser and when it is not able to load (as the component is not there)- it throws this error.

We can use Suspense to resolve this.
Suspense component will has a fallback attribute - which is what will React render when the code is not there. (kind of a loading screen), take in a component.
