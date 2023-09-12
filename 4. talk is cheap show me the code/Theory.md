### What are props?

When we have to dynamically pass in data to our components we pass in as props . They are just like arguments to a func

### What is config driven ui?

### What is optional chaining?

### Why do we need key prop ?

When you have a list of items that is being rendered by react and suppose a new addition comes in, React will not be able to identify the new addition and it will just cleans the container and rerender all of the items again.

But if we provide key's to our list of items while mapping over them - React becomes aware of the items already present in the list and will only render the item with the new id.

### Why we shouldn't use index as key?

It works fine but not recommended.

### Default exports & Named exports

Default exports are fine- but 1 file can have a single default export
