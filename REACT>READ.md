What is 1React?
React is an open-source front-end JavaScript library used to build user interfaces, especially for single-page applications (SPAs). React helps make websites fast, interactive, and easy to manage.
	What are the 1features of React?
•	JSX: A JavaScript syntax extension that allows writing HTML structures in the same file as JavaScript code.
•	Components: Building blocks of React applications; they split the UI into independent, reusable parts.
•	Virtual DOM: React keeps a virtual representation of the real DOM in the memory, and that is known as the virtual DOM. React updates only the changed parts instead of the entire DOM.
•	One-way Data Binding: Ensures a unidirectional data flow, making apps modular and easier to debug.
•	High Performance: React updates only necessary components, improving speed and efficiency.

Why use React 1instead of other frameworks, like Angular?
Easy creation of dynamic applications: React makes it easier to create dynamic web applications because it provides less coding and provides more functionality, whereas, with JavaScript applications, code tends to get complex very quickly.
Improved performance: React uses virtual DOM, which makes web applications perform faster. Virtual DOM compares its previous state and updates only those components in the real DOM, whose states have changed, rather than updating all the components — like conventional web applications.
Reusable components: Components are the building blocks of any React application, and a single app usually consists of multiple components. These components have their own logic and controls, and they can be reused through the application, which, in turn, dramatically reduces the development time of an application.
Unidirectional data flow: React follows a unidirectional data flow. This means that when designing a React app, we often nest child components within parent components. And since the data flows in a single direction, it becomes easier to debug errors and know where the problem occurs in an application at the moment.
Dedicated tools for easy debugging: Facebook has released a chrome extension that we can use to debug React applications. This makes the process of debugging React to web applications faster and easier.


What is 1Virtual DOM?
React is a virtual(lightweight) representation of the real DOM in the memory, and that is known as the virtual DOM.
Virtual DOM provides an abstraction of the actual HTML DOM.
When an object’s state changes, React updates only that object in the real DOM instead of re-rendering the entire DOM.

How the Virtual DOM works in React?
React update the state changes in Virtual DOM first and then it syncs with Real DOM. 
Virtual DOM is just like a blueprint of a machine, can do changes in the blueprint but those changes will not directly apply to the machine.

How Virtual DOM improves performance compared to directly manipulating the real DOM?
•	React batches multiple updates together before applying them to the real DOM, reducing unnecessary re-renders.
•	It only updates the specific components or elements that have changed, minimizing DOM manipulations.
•	React’s efficient diffing algorithm identifies the minimal set of changes needed between the previous and new Virtual DOM representations.
•	React’s reconciliation process optimizes updates by reusing existing DOM elements when possible.

What are 1Controlled components and 1Uncontrolled components?
Controlled Components:
- State is managed by React through props.
- Values and changes are handled through props and event handlers.
- Provides a single source of truth.
- Examples: input fields, checkboxes, select dropdowns.
Uncontrolled Components:
- State is managed internally by the DOM.
- Values and changes are accessed directly from the DOM using techniques like `ref`.
- Offers more flexibility and direct access to the DOM.
- Examples: file inputs, certain form fields.
Controlled: React state controls the value.
Uncontrolled: the DOM holds the value (use ref).

What are the 1Components in React?
React components are reusable, independent pieces of UI. They accept props, manage state, and return JSX that describes the UI. 
Components can be functional or class-based, but functional components with hooks are standard today. 
React applications are built by composing many small components together.
1.	Functional 
2.	Class
1Functional Components: 
Written as JavaScript functions 
Use hooks (useState, useEffect, etc.) 
Lightweight and most commonly used in real projects
// I have worked on functional component not class component

What are 1Pure components?
Pure components in React are components that only re-render when their props or state change.
It automatically implements a shallow comparison of props and state.  
It checks if the new data is different from the old one, and if not, it skips re-rendering. This makes your app faster because it avoids doing extra work.

What is 1state in React?
The state is a built-in React object that is used to contain data or information about the component. The state in a component can change over time, and whenever the state changes, React automatically re-renders the component to show the updated data.
We can update the state of a component by using setState() method

How do you manage state at scale?
Start with React state and context. Use Redux RTK(redux tool kit) or Zustand when state is shared widely or needs caching

What are 1props in React?
Props (short for properties) are a mechanism for passing data from a parent component to its child components
They are read-only, meaning the child component cannot change them—props are just like arguments you give to a function. In simple terms, props help components share data and stay reusable.
Explain React state and props.

How do you handle error boundaries in React?
I use class components with componentDidCatch or libraries like react-error-boundary to catch UI errors and show fallback UI.

What is an 1Event in React?
Events are triggered whenever certain actions occur — such as pressing a key, a mouse click, hovering, focusing form inputs, typing in an input field, or scrolling the page and so on, which then fire off callback functions so that appropriate responses can be made accordingly.

What are the Event 1Handlers in React ?
Event handlers are your own functions that is called when an event occurs. Event handlers are typically defined as props on React components. (To handle an event in React)
•	You can handle events by passing a function as a prop to an element like <button>.
•	Event handlers are defined inside a component, so they can access props.
•	You can declare an event handler in a parent and pass it as a prop to a child.

export default function Button() {
  function handleClick() {
    alert('You clicked me!');
  }

  return (
    <button onClick={handleClick}>
      Click me
    </button>
  );
}
How to Handle 1Errors in React Applications?
Render-time errors: When rendering components (including lifecycle/render functions).
↳ Handled by Error Boundaries. 
Event handler errors: Inside onClick/onChange, etc.
↳ Handled by try/catch (no Error Boundary capture). 
Async errors: fetch, timers, async effects.
↳ Handled by try/catch, .catch, or error states; Error Boundaries don’t catch these. 
Data/validation errors: Invalid inputs, server validation.
↳ Handled via UI state and form libraries. 
Routing-level errors: 404/loader/action errors.
↳ Handled by Router error boundaries (React Router). 
Suspense/streaming: Data fetching + Suspense errors.
↳ Handled by Error Boundaries + Suspense fallback.

Explain 1conditional rendering in React?
Conditional rendering in React allows you to display different content or components based on certain conditions. You can conditionally render JSX using JavaScript syntax like if statements, &&, and ? : operators and switch statement.

How do you avoid unnecessary re-renders?
Use React.memo, useMemo, useCallback, and keep state as small and local as possible.

How do you handle side effects?
Use useEffect and cleanup with a return function. 
Example:
useEffect(() => {
const id = setInterval(fetchData, 5000);
return () => clearInterval(id);
}, []);

How to optimize large lists?
List virtualization (react-window), key props, memoization, and lazy loading.

How do you handle forms?
Use libraries like React Hook Form for performance and validation.
In React, forms are handled using controlled components.
•	You store form data in component state using useState (or in a parent/global state).
•	Each input’s value is bound to state, and you update state on every onChange event.
•	This keeps the UI and data in sync and makes validation easy.
•	For more complex forms, libraries like Formik or React Hook Form help by managing state, validation, and performance.
Example:
const [name, setName] = useState("");
<input 
  value={name} 
  onChange={(e) => setName(e.target.value)} 
/>
inShorts - React handles forms by controlling input values through state, updating state on change, and processing data on submit.

React Hook Form handles forms using uncontrolled inputs with refs, which makes it lightweight and highly performant.
•	You register each input using register, and React Hook Form tracks values without continuously re-rendering.
•	Validation is built in, supports schema validation (e.g., Yup/Zod), and runs efficiently.
•	Submission is handled with handleSubmit, which gives you validated form data.
•	It reduces boilerplate compared to controlled components and improves performance in large forms.
Example - 
const { register, handleSubmit, formState: { errors } } = useForm();
const onSubmit = (data) => console.log(data);
<form onSubmit={handleSubmit(onSubmit)}>
  <input {...register("email", { required: "Email is required" })} />
  {errors.email && <p>{errors.email.message}</p>}
  <button type="submit">Submit</button>
</form>
InShorts - React Hook Form uses uncontrolled inputs with refs, minimizes re-renders, provides easy validation, and simplifies form management in React apps.

What is the 1callback?
A function that you pass from a parent component to a child component, so the child can call it later.
It allows for communication between different components in React.
We use callbacks when:
•	A child component needs to send data to the parent
•	A child needs to notify the parent about something (button click, form submit, etc.)
A callback is a function that is passed as an argument to another function and is executed after a certain event or condition is met. Callbacks are commonly used in React for handling events, managing state updates, and performing asynchronous operations.

What is callback function?
Let's consider a simple example where we have a button that, when clicked, increments a counter. We'll use a callback function to update the state based on the previous state.
Example: Counter with Callback
import React, { useState } from 'react';
const Counter = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    // Using a callback to update the state based on the previous state
    setCount((prevCount) => prevCount + 1);
  };

  const decrement = () => {
    // Using a callback to update the state based on the previous state
    setCount((prevCount) => prevCount - 1);
  };

  const reset = () => {
    setCount(0);
  };

  return (
    <div>
      <h1>{count}</h1>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
      <button onClick={reset}>Reset</button>
    </div>
  );
};
export default Counter;

What is 1Webpack in ReactJS?
When you're working with React, your app can have a lot of files (e.g., JavaScript files, CSS files, images, etc.), and Webpack helps combine all of these into smaller, optimized files that are quicker to load in the browser. It also supports things like code splitting, making sure only the code the user needs is loaded.

How to optimize the 1performance of React app?
•	1. Code Splitting:  Split your code into smaller chunks using tools like Webpack OR Load code in parts using React.lazy and Suspense to speed up initial load.   
•	2. Bundle Size Reduction: Minify and compress JavaScript and CSS to reduce the overall bundle size. Webpack or Babel can help achieve this.
•	3. Lazy Loading: Load components and resources only when they are needed, improving initial load time and reducing data transferred. React.lazy() to load only what is necessary for each page or component.
•	4. Image Optimization: Compress and optimize images to reduce their file size. Tools like ImageOptim or Webpack plugins can assist with this.
•	5. Memoization: Use React’s `React.memo` or `PureComponent` to memoize components and prevent unnecessary re-renders when props or state haven’t changed.
•	6. Virtualization: For long lists, use libraries like `react-virtualized` or `react-window` to render only the visible items, improving performance.
•	7. Avoid Unnecessary Renders: Implement `React.memo` to prevent unnecessary re-renders of components when props haven’t changed.
•	8. Code Profiling: Use tools like React DevTools or Chrome DevTools to identify performance bottlenecks, analyze component render times, and identify slow components.
•	9. Server-Side Rendering (SSR): Implement SSR to pre-render React components on the server, reducing initial load time and improving SEO.
•	10. Caching: Utilize caching mechanisms like HTTP caching or memoization to avoid redundant network requests or calculations.
•	11. Optimize Network Requests: Minimize HTTP requests by combining and compressing resources, using techniques like HTTP/2 or lazy loading.
•	12. Code Optimization: Optimize your code by removing unused dependencies, reducing unnecessary calculations, and avoiding unnecessary DOM manipulations.
•	13. Performance Monitoring: Continuously monitor your app’s performance using tools like Lighthouse, WebPageTest, or New Relic to identify areas for improvement.
I use React.memo to avoid re-renders, split code with React.lazy, and use tools like Chrome DevTools and React Profiler to find slow components. I also avoid passing new props unnecessarily and keep state local when possible.

How to 1Secure Your React.js Application
1.	HTTPS: Ensure your application is served over HTTPS to encrypt data transmitted between the client and server, preventing attackers from intercepting sensitive information.
2.	Avoid Storing Sensitive Data: Avoid storing sensitive information such as passwords, API keys, and tokens directly in your code or client-side storage. Instead, use environment variables or server-side storage solutions.
3.	Implement Authentication: Implement secure authentication mechanisms such as JWT (JSON Web Tokens), OAuth, or session-based authentication to verify the identity of users accessing your application.
4.	Authorization: Enforce proper authorization checks on both the client and server to ensure that users only have access to resources they are authorized to access.
5.	Sanitize Inputs: Protect against XSS attacks by sanitizing and validating user inputs to prevent malicious scripts from being executed in the browser.
6.	Avoid Inline Scripts: Avoid using inline scripts or dynamically generating JavaScript code from user input, as it can introduce security vulnerabilities.
7.	Content Security Policy (CSP): Implement a Content Security Policy to mitigate XSS attacks by specifying which resources can be loaded and executed by your application.
8.	HTTP Headers: Set appropriate HTTP security headers such as X-Content-Type-Options, X-Frame-Options, and X-XSS-Protection to enhance security and prevent common attacks.
9.	Use Libraries dependencies Carefully: Only use well-maintained and secure third-party libraries and dependencies in your application. Keep them updated to mitigate known vulnerabilities.
10.	Secure APIs: Ensure that your backend APIs are secure by implementing proper authentication, authorization, input validation, and rate limiting.
11.	Monitor and Logging: Implement logging and monitoring mechanisms to detect and respond to security incidents, such as unusual activity or unauthorized access attempts.

https://www.youtube.com/watch?v=AcYF18oGn6Y
Explain the 1lifecycle methods of components.
Mounting: This phase occurs when the component is initially rendered and added to the DOM.
Updating: This phase occurs when the component’s state or props change, causing a re-render. It receives new props or state, usually in response to an interaction.
Unmounting: This phase occurs when the component is removed from the DOM.
•	getInitialState(): This is executed before the creation of the component.
•	componentDidMount(): Is executed when the component gets rendered and placed on the DOM.
•	shouldComponentUpdate(): Is invoked when a component determines changes to the DOM and returns a “true” or “false” value based on certain conditions.
•	componentDidUpdate(): Is invoked immediately after rendering takes place.
•	componentWillUnmount(): Is invoked immediately before a component is destroyed and unmounted permanently.
What is React 1Router?
React Router enables smooth, component-based navigation in React apps by handling routing on the client side.
•	It manages navigation without full page reloads.
•	Uses components like BrowserRouter, Routes, and Route to map URLs to UI components.
•	Supports dynamic routes, nested routing, navigation (useNavigate), and route-based data loading.

Why do we need to React Router?
•	It maintains consistent structure and behavior and is used to develop single-page web applications. 
•	Enables multiple views in a single application by defining multiple routes in the React application

What are 1keys in React?
A key is a special string attribute that needs to be included when using lists of elements.

What is a 1higher-order component in React? What, Why, When, How?
Higher-order components (HOCs) are a pattern in React that allows you to reuse component logic by wrapping components with other components.
A higher-order component acts as a container for other components. 
They are generally used when multiple components have to use common logic. 
Use Case:
•	Code Reusability: Extract common logic and reuse it across multiple components.
•	Props Manipulation: Modify or pass additional props to the wrapped component.
•	Rendering Control: Conditionally render the wrapped component based on specific conditions. (Render hijacking)
•	Performance Optimization: Optimize rendering by implementing memorization or caching techniques.
•	Context Manipulation: Provide or consume context to share data or behavior between components. State abstraction and manipulation.
•	Wrap and enhance functionality from third-party libraries.

function withLogger(WrappedComponent) {
  return function WithLogger(props) {
    console.log('Component rendered:', WrappedComponent.name);
    return <WrappedComponent {...props} />;
  };
}

function MyComponent(props) {
  // Component implementation
}

const EnhancedComponent = withLogger(MyComponent); //HOC


What is 1Redux?
Redux is an open-source, JavaScript library used to manage the application state. 
Centralized state management system i.e. Store: Redux state, is stored globally in the store. All the components of the entire application can easily access the data directly. This centralizes all data and makes it very easy for a component to get the state it requires. So while developing large, complex applications with many components, the Redux store is highly preferred.
RTK tool for check data.
Performance Optimizations: Redux store helps in improving the performance by skipping unnecessary re-renders and ensuring that a given component re-renders only when its data has actually changed.

What are the components of Redux?
•	Store: Holds the state of the application.
•	Action: The source information for the store.
•	Reducer: Specifies how the application's state changes in response to actions sent to the store.

import { createStore } from 'redux';

const reducer = (state = 0, action) => {
  if (action.type === 'INCREMENT') {
    return state + 1;
  } else if (action.type === 'DECREMENT') {
    return state - 1;
  }

  return state;
};

const store = createStore(reducer);

store.subscribe(() => {
  console.log('current state', store.getState());
});

store.dispatch({
  type: 'INCREMENT'
});

store.dispatch({
  type: 'INCREMENT'
});


What is 1Zustand?
Zustand is a small, fast, lightweight and flexible state management library for React that avoids boilerplate, provides a simple hook-based API, and offers excellent performance through selective subscriptions.
Many teams prefer it as a more minimal and flexible alternative to Redux.

When to use Zustand over Redux
Use Zustand when you want:
•	Global state with less setup
•	Better performance without complex patterns
•	Easy-to-read, intuitive state logic
•	A small and manageable store
Redux is better when:
•	Your application is huge
•	You require strict immutability and predictability
•	You want large ecosystem tooling

What’s 1Hooks in ReactJS, explain the types of hooks?
This hooks like some utility functions so we can create some dynamic variables
Important: 
•	useState, 
•	useEffect, 
•	useContext, 
•	useReducer, 
•	useMemo, 
•	useCallback, 
•	useRef,

1useState -
The useState() is a built-in React Hook that allows you to have state variables in functional components.

1useEffect hooks. 1effect -
It allows you to handle lifecycle events and perform actions such as fetching data, subscribing to events, or manipulating the DOM.
•	The useEffect hook takes two arguments: a callback function and a dependency array.
•	The callback function is executed after every render of the component.
•	No dependency passed: Runs on every render
•	An empty array: Runs only on the first render
•	Props or state values: Runs on the first render and any time any dependency value changes

1useContext: 
Allows you to consume context in functional components. It accepts a context object (created with React.createContext) and returns the current context value for that context.
Context provides a way to pass data through the component tree without having to pass props manually at every level.

1useReducer: Alternative to useState for managing more complex state logic. It accepts a reducer function and an initial state, returning the current state and a dispatch function to trigger state updates.
1useMemo: The useMemo hook is used to memoize the result of a function. It takes a function and an array of dependencies and returns a memoized value. This is particularly useful when you have expensive computations or calculations that you want to avoid repeating unnecessarily.
In React, useMemo is a hook that helps to optimize performance by memoizing the result of a computation. This means it will only recompute the memoized value when one of its dependencies changes. 
Why use useMemo? 
1.	Avoid expensive recalculation 
2.	Prevent unnecessary renders
Example :
// Expensive calculation
  const expensiveCalculation = (num) => {
    console.log('Calculating...');
    let result = 0;
    for (let i = 0; i < 1000000000; i++) {
      result += num;
    }
    return result;
  };
  // Memoizing the calculation
  const memoizedValue = useMemo(() => expensiveCalculation(count), [count]);

1useCallback: 
1.	The useCallback hook is used to memoize callbacks. 
2.	It takes a callback function and an array of dependencies and returns a memoized callback. 
3.	This is beneficial in scenarios where passing callbacks to child components might cause unnecessary re-renders.
Note: In computing, memoization is used to speed up computer programs by eliminating the repetitive computation of results, and by avoiding repeated calls to functions that process the same input.

What is the difference between useMemo and useCallback, and when not to use them?
useMemo
•	What it memoizes: a value
•	Use case: avoid re-computing expensive calculations
const filteredList = useMemo(() => computeList(data), [data]);
useCallback
•	What it memoizes: a function
•	Use case: avoid re-creating functions passed to child components
const handleClick = useCallback(() => {
  setCount(c => c + 1);
}, []);

Key difference (one line)
useMemo memoizes results, useCallback memoizes functions.

How does 1Suspense work, and what are some real use cases beyond lazy loading
Suspense lets React pause rendering until async work finishes, enabling cleaner loading states, progressive rendering, smoother transitions, and streaming SSR—not just lazy loading.
<Suspense fallback={<Spinner />}>
  <Profile />
</Suspense>
How it works internally (high level):
•	A component suspends by throwing a Promise
•	React pauses rendering that part of the tree
•	Shows the nearest fallback
•	When the Promise resolves, React resumes rendering
Real use cases beyond lazy loading
1.	Data fetching
•	Works with libraries like React Query, Relay, Next.js App Router
•	Enables declarative loading states
<Suspense fallback={<Skeleton />}>
  <UserDetails />
</Suspense>
________________________________________
2.	Progressive rendering
•	Different parts of the page load independently
•	Faster perceived performance
<Suspense fallback={<SidebarSkeleton />}>
  <Sidebar />
</Suspense>
<Suspense fallback={<FeedSkeleton />}>
  <Feed />
</Suspense>

3.	Page transitions
•	Combined with startTransition
•	Keeps old UI visible while new content loads
Benefit: smoother navigation, no blank screens

4.	Streaming Server-Side Rendering (SSR)
•	Server sends HTML in chunks
•	Suspended parts stream later
Benefit: faster time-to-first-content

5.	Error handling with Error Boundaries
•	Suspense handles loading
•	Error boundaries handle failures
Clean separation of concerns
When NOT to use Suspense
•	Simple loading states
•	Legacy data-fetching patterns
•	Without Suspense-compatible libraries

What does memoization mean in React?
Memoization is an optimization technique where React remembers the previous render output of a component and reuses it if the inputs (props) are the same. This avoids unnecessary re-renders and improves performance.

What are 1Custom Hooks?
•	Custom hooks in ReactJS are functions that allow you to extract component logic into reusable functions. 
•	They are a way to share logic between components without having to duplicate code or rely on higher-order components or render props 

The disadvantage of Custom Hooks is it cannot be used inside of the classes.
// for create Localhost storage
In above example [value] is dependency array;

What is Micro Frontend?
The extended concept of microservices in the world of frontend is called micro frontend.
A microfrontend is a development architecture that breaks a product into smaller development units. Each application part exists separately; you can develop, test, and deploy it independently.

What is Context API and when should you use it?
Answer:
Context API lets you share data across components without passing props manually. I use it for global data like theme, user info, or language settings. For complex state, I prefer Redux or Zustand.

How to 1pass state 1data from one component to another component?
1.	Parent to Child (via props)
A parent component can pass its state down to its children as properties, commonly referred to as “props”.
2.	Child to Parent (via callback functions)
To pass data from a child component up to a parent, you can pass a callback function from the parent to the child as a prop. The child then calls this function with the data as an argument.
3.	Sibling to Sibling (share state)
When two components are siblings and they need to share state, you can’t pass the data directly between them. Instead, you lift the state up to their closest common ancestor, which then manages the state and passes it down to both siblings.
4.	Using Context API / Redux / Zustand
React’s Context API allows you to share values like state between components without having to explicitly pass a prop through every level of the tree.
5.	Using State Management Libraries
These examples use hooks like useState, useContext, and Redux hooks like useSelector and useDispatch, which are commonly used in functional components to manage state and context.
import React from 'react';
import { useSelector, useDispatch } from 'react-redux';

// Assuming you have a Redux store and a slice of state called 'dataState'
function Component() {
  // Access state from the Redux store
  const data = useSelector((state) => state.dataState.data);
  const dispatch = useDispatch();

  // Dispatch an action to update the state
  const updateData = (newData) => {
    dispatch({ type: 'UPDATE_DATA', payload: newData });
  };

  return (
    <div>
      <div>{data}</div>
      <button onClick={() => updateData('new data')}>Update Data</button>
    </div>
  );
}

What is the Prop 1drilling in reactjs?
Prop drilling is a term used in React to describe the process of passing data from a part of a component tree to another part by going through other components that do not necessarily need the data, but only pass it down the tree.

Scenario Q&A
1) Scenario: The dashboard is slow after adding filters and charts.
Question: How do you diagnose and fix performance issues?
Answer:
•	Diagnose: Use React Profiler and Chrome DevTools to find components re-rendering often. Check prop changes and state shape.
•	Fix: 
o	Memoize heavy components: React.memo, useMemo for computed values.
o	Stabilize callbacks with useCallback.
o	Split code with React.lazy for routes/charts.
o	Virtualize large tables (react-window).
o	Move global state out of frequently re-rendered parents.
•	Metric: Reduced initial load from 4s to 1.8s, interaction delay from 300ms to 50ms.

I) Scenario: Your React app suddenly becomes slow after adding new features. How do you find and fix the issue?
Question: How do you diagnose and fix performance issues?
Answer: 
1. Chrome dev tools -> performance tab
2. React devtool -> check unnecessary re-renders
3. memo, usCallback
4. virtualization -> react window
5. Avoid inline functions/objects

2) Scenario: Form with dynamic fields has validation lag and lost input.
Question: What would you do?
Answer:
•	Switch to React Hook Form for controlled+uncontrolled hybrid performance.
•	Use schema validation (Yup/Zod) for clean rules.
•	Debounce API validations (e.g., email uniqueness) to avoid spam calls.
•	Keep form state local to avoid global re-renders.

 Scenario: How do you prevent a login page from being accessible after the user is logged in?
Question: What would you do?
Answer: - 
3.	Protected Routes 
4.	Context- redux 
5.	Router -> login

Scenario: A component fetching the same data multiple times unnecessary. How do you fix?
Question: What would you do?
Answer – 
1.	React Query -> caching
2.	Store data in Context / Redux / Zustand 
3.	usMemo

Scenario: How do you optimize bundle size in a large React?
Question: What would you do?
Answer – 
1.	code splitting -> React lazy, suspense
2.	Tree shaking -> vite, webpack (it unused imports)
3.	Dynamic imports
4.	Compress assets
5.	Caching – user device

Scenario: How do you handle a form with 20+ fields efficiently?
Question: What would you do?
Answer – 
1.	React hook form / formik
2.	Steps / logical sections
3.	Controller components -> state, value onchange
4.	Conditional / dynamic render
5.	Zod -> validation

Scenario: You app needs to support dark mode. How do you implement it?
Question: What would you do?
Answer – 
1.	User / system -> prefer color scheme -> localstorage store theme
2.	Redux / context API -> provider 
3.	Css variables / tailwind css -> tokens

Scenario: How do you prevent XSS(cross site scripting) in frontend apps?
Answer – 
1.	Sanitization - Dom purify for sanitize
2.	CSP – content security policy header

Scenario: How do you handle online/offline state gracefully in React with service workers?
Answer – 
1.	Navigator.onLine -> provided by browser
2.	By service worker -> use cache if user offline. It is kind on PWA(progressive web app) 

Scenario: production is not getting the latest deployed update unless in incognito. How do you solve this?
Answer – 
1.	Check Service worker -> always store the cache 
2.	Static assets  like chunks. Hashing -> it will replace chunk name
3.	Cache control headers -> no-cache, must-revalidate kind of headers
4.	App version meta deta pass
 
Q1. What causes a memory leak in a React component using useEffect ? 
Ans-
1.	No cleanup -> Stale references stay in memory
2.	Return cleanup function in useEffect
3.	Common culprit -> Setinterval, event listner, subscription
4.	React warning -> “Can’t perform a state operate on unmounted component”

Q2. How can API calls cause memory leaks in React?
Ans-
1.	Component unmount before API resolve
2.	setState() in unmounted component = leak
3.	use AbortController to pending request
4.	check isMounted before updating state  

Q3. How do prevent event listeners create a memory leak in react?
Ans – 
1.	Multiple listeners = multiple closures in memory
2.	Always remove listeners in cleanup
3.	Window.addEventListeners -> removeEventListener
4.	Repeak re-renders = exponential leaks

Q. What are concurrent features in react and how do you they help?
Concurrent React lets React prioritize urgent updates and delay heavy work to keep apps fast and responsive.
Key concurrent features (React 18):
•	Concurrent Rendering: Rendering is interruptible, so React can pause or stop work to keep the UI responsive.
•	Transitions (startTransition, useTransition): Mark non-urgent updates so urgent actions like typing stay fast.
•	useDeferredValue: Defers expensive updates to avoid UI lag.
•	Suspense (enhanced): Allows components to wait for data/code and show fallback UI smoothly.
•	Automatic Batching: Groups multiple state updates into a single render for better performance.
How they help:
•	Prevent UI freezes
•	Improve responsiveness
•	Enable smoother loading and navigation
•	Improve perceived performance

Q. Explain timer in event loop?
In the browser, JavaScript runs in a single thread. The event loop coordinates:
•	Call Stack → where JS runs your code
•	Web APIs → where timers (setTimeout, setInterval), DOM events, fetch, etc. wait
•	Task Queues 
o	Macrotasks → timers, DOM events
o	Microtasks → Promise.then, .catch, .finally, queueMicrotask, MutationObserver (these run before timers)
Key rule: After your current code finishes, the browser first runs microtasks, then timers (macrotasks).

Q. Explain React’s Batching behavior and what changed in React 18.
What is batching in React?
Batching is when React groups multiple state updates into a single render to improve performance.
Before React 18
•	Batching worked only inside React event handlers
•	Updates in setTimeout, promises, or async code caused multiple renders
React 18 (What changed)
•	Automatic batching everywhere
•	Updates are batched in:
o	Event handlers
o	setTimeout
o	Promises
o	Async/await
o	Native event listeners
setTimeout(() => {
  setCount(c => c + 1);
  setFlag(true);
  // ✅ One render in React 18   // ❌ Two renders before React 18
}, 1000);

Q4 . Can closure or refs cause memory leak in React? 
Yes, closures and refs can cause memory leaks in React if they keep references to objects that are no longer needed.
Closures
•	 A closure in React means a function remembers the state/props from the moment it was created, even if things change later.
•	Closures capture variables from their scope.
•	A memory leak can happen if:
o	An effect or callback keeps a reference to large data or DOM nodes
o	Event listeners, intervals, or subscriptions are not cleaned up
Example cause
•	setInterval, event listeners, or async callbacks without cleanup
Prevention
•	Always clean up in useEffect
•	Avoid capturing unnecessary variables

Refs (useRef)
•	Refs persist across renders and do not get garbage collected while the component is mounted.
•	A memory leak can happen if:
o	Refs store large objects, DOM nodes, or external resources
o	They are not cleared on unmount
Prevention
•	Use refs only when needed
•	Clear refs in cleanup (ref.current = null)


3) Scenario: Feature flag toggling causes parts of UI to break.
Question: How do you prevent runtime UI errors?
Answer:
•	Wrap risky UI parts in Error Boundaries with fallbacks.
•	Add contract tests for feature flag combinations.
•	Use feature flag defaults and safe fallbacks on fetch failures.


Coding Que

Below is a simple React component that includes an input field and a button. When you enter text into the input field and click the button, the text will be added to a list displayed below the input.
Simple Input Field with List

Explanation:
1.	State Management:
•	We use the useState hook to manage two pieces of state: inputValue (to hold the current value of the input field) and items (to hold the list of items).
2.	Input Field:
•	The input field is controlled by the inputValue state. The onChange event updates the inputValue state whenever the user types in the input field.
3.	Add Button:
•	The handleAddItem function is called when the button is clicked. It checks if the input is not empty, adds the inputValue to the items array, and then clears the input field.
4.	Display List:
•	The list of items is displayed using the map function, which iterates over the items array and renders each item in a <li> element.


Run locally project-
Npm run dev 

Components are UI building block.
 

State management (All about data)
Share State
Props
Props Drilling
Context API

Redux?
Custom Hooks?
Lazy loading – code splitting, chunking, suspense

Lazy Loading -
Load components and resources only when they are needed, improving initial load time and reducing data transferred.

SSR vs CSR? Server/client side rendering

Routing? (Role based access control)
Protected routes?
Dynamic routing?
Testing? (Unit testing)
	React testing library
	
Async tasks? 
	API calls
	Events
	Promises

Keywords – Reusable, testable, modularity, readable
Performance
	Shimer UI
	Lazy loading
	Asset optimization – JS, CSS
	Bundler code
	CDAN / server
	Rendering components
Styling
	Tailwind
	styleX - facebook
	Bootstrap
	Material UI
Accessibility
Security 	

Improving your skills as a ReactJS developer can be both exciting and rewarding. Here are some tips to help you enhance your expertise:
1.	Deepen Your Understanding of JavaScript: Since React is built on JavaScript, having a strong grasp of ES6+ features (like arrow functions, destructuring, spread/rest operators, and async/await) is crucial.
2.	Master React Fundamentals: Ensure you have a solid understanding of React concepts such as components, props, state, lifecycle methods, and hooks (like useState, useEffect, and custom hooks).
3.	Explore Advanced Patterns: Learn about higher-order components, render props, and context API. Understanding these patterns can help you write more reusable and maintainable code.
4.	State Management: Familiarize yourself with state management libraries like Redux, MobX, or the Context API. Understanding when and how to use these tools is essential for larger applications.
5.	TypeScript: Consider learning TypeScript, as it can help you write more robust and maintainable code by adding static typing to your JavaScript.
6.	Testing: Learn how to write tests for your React components using tools like Jest and React Testing Library. Testing is crucial for ensuring the reliability of your applications.
7.	Performance Optimization: Understand how to optimize your React applications for performance. Learn about techniques like memoization, lazy loading, and code splitting.
8.	Build Real Projects: Apply your knowledge by building real-world projects. This could be anything from a personal portfolio to a full-fledged web application. The more you practice, the better you'll get.
9.	Stay Updated: React is constantly evolving. Follow the official React blog, subscribe to newsletters, and participate in community forums to stay updated on the latest features and best practices.
10.	Contribute to Open Source: Contributing to open-source projects can provide valuable experience and expose you to different coding styles and practices.
11.	Join the Community: Engage with the React community through forums, social media, or local meetups. Networking with other developers can provide support and new insights.
12.	Read Documentation: The official React documentation is a great resource. Make it a habit to read through it regularly, especially when new features are released.
By focusing on these areas, you'll be well on your way to becoming a more proficient ReactJS developer. 
Happy coding!


1.	Create a Simple Counter App:
•	Build a counter application that allows users to increment, decrement, and reset the counter value. Use React hooks for state management.
2.	Todo List Application:
•	Create a todo list app where users can add, delete, and mark tasks as completed. Implement local storage to persist the todos even after a page refresh.
3.	Fetch and Display Data:
•	Build a component that fetches data from a public API (like JSONPlaceholder) and displays it in a list. Handle loading and error states appropriately.
4.	Form Handling:
•	Create a form that collects user information (name, email, and message). Validate the inputs and display error messages for invalid entries.
5.	Dynamic Routing:
•	Use React Router to create a multi-page application. Implement dynamic routing to display user profiles based on a user ID passed in the URL.
6.	Image Gallery:
•	Build an image gallery that fetches images from an API (like Unsplash) and displays them in a grid. Implement a modal to view images in a larger format when clicked.
7.	Search Filter:
•	Create a component that takes an array of items (e.g., a list of names) and allows users to filter the list based on their input in a search box.
8.	Pagination:
•	Implement pagination for a list of items. Create a component that fetches data and displays a limited number of items per page, with buttons to navigate between pages.
9.	Drag and Drop:
•	Build a simple drag-and-drop interface where users can reorder a list of items. Use the react-beautiful-dnd library or similar for implementation.
10.	Theme Switcher:
•	Create a theme switcher that allows users to toggle between light and dark modes. Use context or state management to persist the user's choice.
11.	Custom Hook:
•	Write a custom hook that manages form input state. The hook should return the current value, a change handler, and a reset function.
12.	Error Boundary:
•	Implement an error boundary component that catches JavaScript errors in its child components and displays a fallback UI.
13.	Memoization:
•	Create a component that displays a list of items and uses React.memo to prevent unnecessary re-renders when the parent component updates.
14.	Responsive Navigation Bar:
•	Build a responsive navigation bar that collapses into a hamburger menu on smaller screens. Use CSS and React state to manage the open/close state of the menu.
15.	Infinite Scroll:
•	Implement an infinite scroll feature for a list of items. Fetch more items as the user scrolls down the page.
These coding challenges will help you practice various aspects of React development, including state management, component design, API integration, and user interaction. Happy coding!
Give me solutions of all above practice questions
.


1. Simple Counter App
2. 1Todo List Application
. Fetch and Display Data
4. Form Handling

Certainly! You can use a 1callback function with the setCount function in the Simple Counter App to ensure that you're updating the state based on the previous state. This is particularly useful in scenarios where the state update depends on the current state value. Here's how you can modify the Simple Counter App to use a callback:
Simple Counter App with Callback

Explanation:
•	In this version, the increment and decrement functions use the callback form of setCount.
•	The callback receives the previous state (prevCount) as an argument, allowing you to safely update the state based on its current value.
•	This approach is particularly useful in scenarios where multiple state updates might occur in quick succession, ensuring that you always work with the most up-to-date state.
Feel free to implement this in your application!

Notes:
If you want to write 10 div  .div$*10


Sample questions 
What is react reconciliation,
React Closers ,
React timer code and explain,
Questions on Closers,
And basic react Questions,
Hooks and custom hooks
UseState ans function state update, useEffect 


