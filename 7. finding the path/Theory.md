### useEffect Cases:

1. If no dependency array -> useEffect is called on every render.
2. If depenedency array is empty -> called once in initial render.
3. If something is there in dependency array -> called everytime the dependency changes.

### useState

1. Never create useSTate inside the body --> will throw an error
2. Never use useState declarations in if -else - causes inconsisities in pogram --> is valid but not recommeneded

### react-router-dom

- createBrowserRouter: This will create the roting configurations as we provide an array of objects - containing path & element
- RouterProvider: provides the configuration to our app - connected
- useRouteError - gives us properties to show when we are on error page- like error.status , statusText
- Outlet - to load the children routes in the outlet - this outlet will be replaced the componets according to the path. We will not see any "Outlet" component.
- useParams hook - gives us dynamic data from our route like id for restuarats etc

### children-routes:

Say you have header & footer which are fixed for you app but you app's body will change based on the routes
to implement such a functionality we need children routes
WE can use the Outlet component provided by react-router-dom
-We can define the children routes in children property

### React- changing routes

If we want to link another page in homepage- we should not use anchor tags- anchor tags will result to load the whole page and it defeats the purpose of SPA

We can use "Link" component to route to diff components - not result in reload of pages

### React - SPA ( Single Page Application ) - Why?

Everything in react is just components replacing/interchanging each other - we are not refreshing or reloading
the main component again & again - even when we change routes we will not relaod the page.
All this happens via Client Side Routing.

### 2 types of Routing

1. Client Side Routing : we do not need to fetch any data - all the components are present in our app - when a user clicks on a Link tag , that specific component is rendered onto the page
2. Server Side Routing: when user clicks on anchor tag - network call is triggered to fetch data from server and that is rendered onto our page - causes a relaod for the whole process.

### Dynamic Routing

Routing will be changed based on id
