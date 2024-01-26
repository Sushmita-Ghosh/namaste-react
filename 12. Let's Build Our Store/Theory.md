### What is Redux Store?

It is a big object that is accessible global within our application.

### What are slices?

Slices are small portion of Redux store.

### Modifying Slices:

- Redux says we can't directly modify cart slice.
- There is a way - we need to always dispatch an action (calls a reducer function) - modifies a cart slice of our redux store
- Read data from Cart: we use selector- this selector will help modify the react component - subscribing to the store.

### Steps :

1. Install lib- @reduxjs/toolkit and react-redux
2. Build Our Store - configure store
3. Connect our store to our app. - provider
4. create a slice - cartSlice
5. dispatch an action
6. read the data using

### Important Pointers 🎯😲:

- While using selector subscribe to the only needed portion of the store, instead of the whole store - or wrong portion - since it leads to performance loss, because it will subscribe to updates as mentioned.
- When store it is reducer (big one) - for slices it is reducers:
- Redux Toolkit gives us option to modify the state directly unlike redux which used to say ki don't mutate state
- Redux behind the scenes uses immer library to identify these state changes
- Redux does not allow you to read the state directly - creates a ProxyObject - to read the state we need current(state) - current comes from @reduxjs/toolkit lib
