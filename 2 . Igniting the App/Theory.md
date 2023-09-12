### DAY 2 NOTES

- `NPM` behind the scenes acts as node package manager, but it is not the abbreviation - 🤯
- All packages are hosted on `NPM`
- How to add NPM - `npm init`

### What is a bundler?

So our code needs to minified & cached before sending to production - Bundler helps to create bundles of our code before shipping to production
`Webpack`,`Bable`,`Vite`,

- CRA behind the scenes uses webpack.

* There are two 2 type of ddependencies - dev & normal - dev are those which are used for development purposes only. but normal are those which have to be used in production also.

### What is the difference between ~ & ^ in package.json ?

`Tilde` will automatically upgrade your apps to major version - but `Caret` only upgrades to minor versions. So, it is advised to use ^ as ~ might lead to some things breaking in your app.

### What is the difference between package.json & package-lock.json ?

- package-lock.json keeps track of exact versions that the app is using - package.json has approx version numbers.
- There are many other things that come with package-lock file , one os which is `integrity`, this is a hash512 key which verifies that versions in local & production- such that our app does not break on production.

### What is node-modules?

It consists of the actual code that is fetched from npm for the node-modules

### WHat is transitive dependency?

We might wonder whenever we install something like `npm install parcel` - why do extra set of packages exist along with parcel in node-modules. We do not install these explicitely but they come whenever we are installing one package. These are packages which are needed for `parcel` to function & the depenedencies might need some other dependencies to funtion. We need all of them for `parcel` to function. THese are transitive dependency.

### What is npx?

NPX is execute a package

### CDN links are not preferred way of adding react into our code - WHY?

As fetching react from cdn will make a call to unpkg.com- which is a costly operation better to have it in node_modules. Also like when react upgrades comes - we will have to constantly look out for new links , better to have it in package.json . Upgrades are easier to manage that way.

### What does `import React from "react"` mean ?

We are bringing the React Components from react node modules.

### How to fix BrowserScripts cannot have imports or expoxts?

We need to add `type = "module"` to our script tag. Our App.js is not a normal javascript file - but parcel will treat it as it does not contain the type

### HMR

Hot Module Replacement - Means automaticlly refreshed and renders new change when we do some changes in parcel which is achieved by File watching ALgorithm written in C++.

- React is not the only thing that is making our apps fast. We must appreciate the bundlers , cz a lot of stuff is handled by them which in turn makes our app faster.

### What is consistent hashing ?

### What is differential Bundling?

Parcel gives you the ability to have different bundles for different types of apps.

### What is browserList ?

Link:

#### COMMANDS

npx parcel index.html creates our localhost server

### Build Errors

1.

2. Error: Expected content key de1e4a02ec63c4eb to exist : it turned out that Parcel seemingly can't create the cache if it can't find when i was working on project.

Resolution:
You have to first stops the execution of program by ctrl + c.
then you have to delete the .parcel-cache from the project.
then build the project. npx parcel index.html

3. "Warning: You are importing createRoot from 'react-dom' which is not supported. You should instead import it from 'react-dom/client'"

The new ReactDOM comes from 'react-dom/client' - So modify the react-dom to react-dom/client.
