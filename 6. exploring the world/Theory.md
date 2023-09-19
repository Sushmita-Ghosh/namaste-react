### What is Monolith architecture?

Traditionaly or previously all apps were developed using a monolith architecture.
If a project is built using the monolith architecture, it will have API code, UI COde, authentication code, database connectivity, notifications etc all on the same project.

### What is a microservice architecture?

We have different services for different jobs
all the above will be different small services and all of them combined will form the application.
This is known as "separation of concerns", follows a "single responsiility principle" where each service had a different job.

### 2 approaches of fetching data from backend:

- load website --> make call to API --> once fetched the UI renders

As soon as our page loads we can fetch the data & render on to the UI, So say our api fetching data takes 500 ms - so our page will wait for the results( i.e. wait for 500 ms)

- 2nd approach is - load the website/app --> then UI renders (skeleton) --> make api call--> rerender the UI from data from api -

- In React we will always use the second approach - why is it better- looks complicated r8? but this gives
  a better UX.

- In the first approach for the initial 500 ms our app is kind of like frozen- we will suddenly
  In second approach we will see the skeleton - user will not see lag --> even though we are rendering twice--doesn't matter react render cycles are very fast.

### useEffect:

- The callback in useEffect is called after the component renders.
- First the body will be rendered, then only the useEffect callback is called.

### What is CORS policy/ error?

Basically when we try to call the Swiggy Api from our local host we get CORS policy error.
Our browsers block us to call APi from one origin to other origin.

We can use CORS chrome extension to bypass this error

### What is optional chaining?

### What is Shimmer UI?

A shimmer UI is a version of the UI that doesn't contain actual content, but instead mimics the layout and shapes of the content that will eventually appear.
"Skeleton"
