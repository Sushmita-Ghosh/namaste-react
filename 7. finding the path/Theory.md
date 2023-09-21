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

###
