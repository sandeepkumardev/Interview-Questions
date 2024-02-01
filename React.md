<div align="center">
  <img height="60" src="https://img.icons8.com/ultraviolet/80/000000/react--v2.png"/>
  <h1>React Questions</h1>
  
  From basic to advanced: test how well you know React, refresh your knowledge a bit, or prepare for your coding interview! 💪 🚀
</div>

## React Basics:

#### 1. What is React.js?

<details><summary><b>Answer</b></summary>
  React.js is a JavaScript library developed by Facebook for building user interfaces, particularly for single-page applications. It's widely used for its efficiency and flexibility in creating interactive and dynamic UI components.
</details>

#### 2. What are the key features of React.js?

<details><summary><b>Answer</b></summary>
React.js offers several key features:

- **Component-based architecture**: React organizes UI elements into reusable components, enhancing modularity and maintainability.
- **Virtual DOM**: React uses a virtual representation of the DOM for efficient updates, resulting in better performance.
- **JSX (JavaScript XML)**: React allows developers to write UI components using JSX, a syntax extension that combines HTML-like syntax with JavaScript.
- **Unidirectional data flow**: React follows a one-way data flow, ensuring predictable state management and simplifying debugging.
- **Declarative syntax**: React encourages a declarative approach to UI development, enabling developers to describe the desired UI state rather than imperatively manipulating the DOM.
</details>

#### 3. Explain JSX in React.

<details><summary><b>Answer</b></summary>
JSX (JavaScript XML) is a syntax extension used in React that allows developers to write HTML-like code within JavaScript. It provides a more concise and expressive way to define UI components. JSX elements are transpiled into regular JavaScript function calls by tools like Babel before being rendered in the browser.

For example:

```jsx
const element = <h1>Hello, world!</h1>;
This JSX expression gets transpiled to:
```

```javascript
const element = React.createElement("h1", null, "Hello, world!");
```

JSX makes it easier to visualize the structure of UI components and embed JavaScript expressions directly within the markup.

</details>

#### 4. **What is Virtual DOM in React?**

<details><summary><b>Answer</b></summary>

The Virtual DOM in React is a lightweight, in-memory representation of the actual DOM (Document Object Model) of a web page. React uses the Virtual DOM to efficiently update the UI by comparing the current Virtual DOM with a previous version and applying only the necessary changes to the actual DOM. This approach improves performance by minimizing the number of DOM manipulations, resulting in faster rendering and better user experience.

</details>

## Components:

#### 5. **What is a component in React?**

<details><summary><b>Answer</b></summary>

In React, a component is a reusable piece of user interface (UI) that encapsulates a specific set of functionality and renders a portion of the UI. Components can be thought of as building blocks for creating complex user interfaces. There are two main types of components in React:

- **Functional Components:** Also known as stateless components, these are JavaScript functions that accept props (short for properties) as input and return JSX to describe the UI.
- **Class Components:** Also known as stateful components, these are ES6 classes that extend the React.Component class. They have their own state and lifecycle methods, allowing for more complex behavior.

Components can be composed together to build larger UIs, and they promote code reusability, maintainability, and modularity in React applications.

</details>

#### 6. **Explain the difference between functional components and class components.**

<details><summary><b>Answer</b></summary>

- **Functional Components:**

  - Also known as stateless components.
  - Written as JavaScript functions.
  - Accept props (properties) as input and return JSX to describe the UI.
  - Don't have their own internal state or lifecycle methods.
  - Simple and lightweight, ideal for presentational components.
  - Preferred approach for simpler components in modern React applications due to their simplicity and performance benefits.

- **Class Components:**
  - Also known as stateful components.
  - Written as ES6 classes that extend the `React.Component` class.
  - Can hold their own state using `this.state` and manage lifecycle methods like `componentDidMount`, `componentDidUpdate`, etc.
  - Historically used for more complex components that require state management and lifecycle methods.
  - With the introduction of React Hooks, functional components can now handle state and lifecycle events, reducing the need for class components.

In summary, functional components are simpler and primarily used for presentational purposes, while class components offer more features such as state and lifecycle methods, making them suitable for managing complex behavior.

</details>

#### 7. **How do you create a component in React?**

<details><summary><b>Answer</b></summary>

In React, you can create a component by defining either a functional component or a class component.

- **Functional Component:**
  To create a functional component, you define a JavaScript function that returns JSX representing the UI of the component. Here's an example:

  ```jsx
  import React from "react";

  function MyComponent(props) {
    return <div>Hello, {props.name}!</div>;
  }

  export default MyComponent;
  ```

- **Class Component:**
  To create a class component, you define a JavaScript class that extends `React.Component` and implement a `render` method that returns JSX. Here's an example:

  ```jsx
  import React, { Component } from "react";

  class MyComponent extends Component {
    render() {
      return <div>Hello, {this.props.name}!</div>;
    }
  }

  export default MyComponent;
  ```

Once you've defined the component, you can use it by importing it into other components or files and rendering it like any other HTML element. For example:

```jsx
import React from "react";
import MyComponent from "./MyComponent";

function App() {
  return (
    <div>
      <MyComponent name="Alice" />
      <MyComponent name="Bob" />
    </div>
  );
}

export default App;
```

</details>

#### 8. **What are props in React?**

<details><summary><b>Answer</b></summary>

In React, props (short for properties) are a mechanism for passing data from parent components to child components. Props are read-only and help to make components reusable and modular.

- **Passing Props:**
  Parent components can pass data to child components by adding attributes to the child component's JSX tag. These attributes are then accessible within the child component as properties of the `props` object.

- **Using Props:**
  Child components receive props as an object argument to their functional component or as properties of the `this.props` object within a class component. They can then use these props to customize their behavior and render dynamic content.

Example:

```jsx
// ParentComponent.js
import React from 'react';
import ChildComponent from './ChildComponent';

function ParentComponent() {
    return <ChildComponent name="Alice" age={30} />;
}

export default ParentComponent;

// ChildComponent.js
import React from 'react';

function ChildComponent(props) {
    return (
        <div>
            <p>Name: {props.name}</p>
            <p>Age: {props.age}</p>
        </div>
    );
}

export default ChildComponent;
```

In this example, the `name` and `age` props are passed from the `ParentComponent` to the `ChildComponent`, and the `ChildComponent` uses these props to render dynamic content.

</details>

#### 9. **What are stateful and stateless components?**

<details><summary><b>Answer</b></summary>

- **Stateful Components:**

  - Also known as class components.
  - Have their own internal state managed using `this.state`.
  - Can change their state over time in response to user interactions or other factors.
  - Implement lifecycle methods such as `componentDidMount`, `componentDidUpdate`, etc.
  - Historically used for more complex components that require state management and lifecycle methods.

- **Stateless Components:**
  - Also known as functional components.
  - Do not have their own internal state.
  - Receive data via props and render UI based on that data.
  - Pure functions that return JSX based on input props.
  - Simple and lightweight, ideal for presentational components that only rely on props for rendering.

In summary, stateful components manage their own state and have more features, while stateless components are purely based on the input props and are simpler in nature.

</details>

## State and Props:

#### 10. **What is state in React and how is it different from props?**

<details><summary><b>Answer</b></summary>

- **State in React:**

  - State represents the internal data of a component that can change over time.
  - Managed using the `this.state` property in class components.
  - Used to store dynamic data that affects the component's behavior and appearance.
  - Changes to state trigger re-renders, updating the UI to reflect the new state.

- **Props in React:**
  - Props (short for properties) are inputs to a component that are passed from its parent component.
  - Received as an object argument in functional components or as properties of the `this.props` object in class components.
  - Props are read-only and cannot be modified by the component itself.
  - Used to customize the behavior and appearance of a component based on data passed from its parent.

**Key Differences:**

- **Mutability:** State is mutable and managed internally by the component, while props are immutable and passed from parent components.
- **Ownership:** State is owned and managed by the component itself, whereas props are owned and managed by the parent component.
- **Changes:** Changes to state trigger re-renders within the component, while changes to props do not trigger re-renders unless explicitly handled within the component.
- **Usage:** State is used for dynamic data that can change over time within a component, while props are used for passing data from parent to child components.

In summary, state represents internal component data that can change over time, while props represent external data passed to a component from its parent.

</details>

#### 11. **How do you update state in React?**

<details><summary><b>Answer</b></summary>

In React, you update state by calling the `setState()` method provided by the `React.Component` class. This method takes an object as an argument, which represents the new state or a function that returns the new state based on the previous state.

**Class Components:**

```jsx
import React, { Component } from "react";

class MyComponent extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }

  handleClick = () => {
    // Update state using setState
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.handleClick}>Increment</button>
      </div>
    );
  }
}

export default MyComponent;
```

In this example, `setState()` is called within the `handleClick` method to increment the `count` state.

**Functional Components (with Hooks):**

```jsx
import React, { useState } from "react";

function MyComponent() {
  const [count, setCount] = useState(0);

  const handleClick = () => {
    // Update state using setCount
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Increment</button>
    </div>
  );
}

export default MyComponent;
```

In functional components, state is managed using the `useState` hook, and `setCount` is used to update the state.

In both cases, React will schedule a re-render of the component with the updated state, and the UI will reflect the changes accordingly.

</details>

#### 12. **Explain the concept of lifting state up in React.**

<details><summary><b>Answer</b></summary>

Lifting state up is a pattern in React where the state of multiple components is lifted up to their closest common ancestor, typically a parent component. This allows multiple child components to share and synchronize the same state, enabling them to communicate with each other indirectly via props.

**Key Concepts:**

- **Shared State:** By lifting state up to a common ancestor, child components can share the same state and stay synchronized.
- **Unidirectional Data Flow:** State is passed down from parent to child components via props, and changes to the state are propagated back up through callback functions passed down as props.
- **Separation of Concerns:** Lifting state up promotes better separation of concerns by moving state management to higher-level components, making the codebase easier to understand and maintain.
- **Centralized Logic:** State management logic is centralized in the parent component, reducing duplication and making it easier to manage complex state interactions.

**Example:**
Consider a scenario where you have a parent component `App` with two child components `ComponentA` and `ComponentB`. If both `ComponentA` and `ComponentB` need to share and synchronize the same state, you can lift the state up to the `App` component, and pass it down to the child components as props. Any changes to the state can be handled in the `App` component, and the updated state can be passed down to the child components to reflect the changes.

```jsx
// App.js
import React, { useState } from "react";
import ComponentA from "./ComponentA";
import ComponentB from "./ComponentB";

function App() {
  const [sharedState, setSharedState] = useState("");

  const handleChange = (newValue) => {
    // Update the shared state
    setSharedState(newValue);
  };

  return (
    <div>
      <ComponentA sharedState={sharedState} handleChange={handleChange} />
      <ComponentB sharedState={sharedState} handleChange={handleChange} />
    </div>
  );
}

export default App;
```

In this example, the `App` component manages the `sharedState` and passes it down to `ComponentA` and `ComponentB` along with a `handleChange` function to update the state. Both `ComponentA` and `ComponentB` can access and update the shared state through props, ensuring they stay synchronized.

</details>

#### 13. **How do you pass data from parent to child components in React?**

<details><summary><b>Answer</b></summary>

Data can be passed from parent to child components in React by using props (short for properties). Props are passed as attributes in JSX when rendering child components, and they are accessible within the child component as properties of the `props` object.

**Example:**

Parent Component (`ParentComponent.js`):

```jsx
import React from "react";
import ChildComponent from "./ChildComponent";

function ParentComponent() {
  const data = "Hello from parent!";

  return (
    <div>
      <ChildComponent message={data} />
    </div>
  );
}

export default ParentComponent;
```

Child Component (`ChildComponent.js`):

```jsx
import React from "react";

function ChildComponent(props) {
  return (
    <div>
      <p>{props.message}</p>
    </div>
  );
}

export default ChildComponent;
```

In this example, the `ParentComponent` passes the `data` variable as a prop named `message` to the `ChildComponent`. Inside the `ChildComponent`, the prop is accessed using `props.message` and rendered within the JSX.

Props provide a way to pass data from parent to child components and are an essential mechanism for building reusable and modular components in React.

</details>

#### 14. **What are default props in React?**

<details><summary><b>Answer</b></summary>

Default props are a feature in React that allow you to specify default values for props in a component. These default values are used if the component is rendered without providing the corresponding prop or if the prop is explicitly set to `undefined`.

**Example:**

```jsx
import React from "react";

function MyComponent(props) {
  // Define default props
  const { name } = props;
  const defaultName = "Guest";

  return (
    <div>
      <p>Hello, {name || defaultName}!</p>
    </div>
  );
}

// Set default props
MyComponent.defaultProps = {
  name: "Guest",
};

export default MyComponent;
```

In this example, the `MyComponent` defines a default prop `name` with the value `'Guest'`. If the `name` prop is not provided when rendering the component, or if it is explicitly set to `undefined`, the component will use the default value `'Guest'`.

Default props provide a way to ensure that components have sensible default behavior even if certain props are not provided or are provided with invalid values.

</details>

## Lifecycle Methods:

#### 15. **Explain the lifecycle methods of a React component.**

<details><summary><b>Answer</b></summary>

In React 16, the lifecycle methods have been divided into three categories: Mounting, Updating, and Unmounting.

**Mounting:**

1. **constructor(props):** This method is invoked before a component is mounted. It's used for initializing state and binding event handlers. This method is optional.

2. **static getDerivedStateFromProps(props, state):** This static method is invoked right before calling the `render` method, both on the initial mount and on subsequent updates. It's used to update the state based on changes in props. It should return an object to update the state, or null to indicate that the new props do not require any state updates.

3. **render():** This method is responsible for rendering the component's UI based on its current props and state. It returns JSX representing the component's UI.

4. **componentDidMount():** This method is invoked immediately after a component is mounted. It's commonly used for performing side effects such as data fetching, initializing timers, or adding event listeners.

**Updating:**

5. **static getDerivedStateFromProps(nextProps, prevState):** Similar to the `getDerivedStateFromProps` method in Mounting phase, this method is invoked right before calling the `render` method on every update. It's used to update the state based on changes in props. It should return an object to update the state, or null to indicate that the new props do not require any state updates.

6. **shouldComponentUpdate(nextProps, nextState):** This method is invoked before rendering when new props or state are being received. It allows you to control whether the component should re-render or not. By default, it returns true, indicating that the component should re-render. Returning false will prevent the component from re-rendering.

7. **render():** Same as in the Mounting phase, this method is responsible for rendering the component's UI based on its current props and state. It returns JSX representing the component's UI.

8. **componentDidUpdate(prevProps, prevState):** This method is invoked immediately after updating occurs. It's useful for performing side effects based on changes to props or state. However, you should be cautious when using it to avoid causing infinite loops by updating state within this method.

**Unmounting:**

9. **componentWillUnmount():** This method is invoked immediately before a component is unmounted and destroyed. It's used for cleanup tasks such as removing event listeners or canceling timers.

These lifecycle methods provide developers with hooks to perform actions at various stages of a component's lifecycle, allowing for more control and customization of component behavior. However, it's essential to understand when and how to use them appropriately to avoid potential issues such as memory leaks or performance problems.

In React Hooks, lifecycle methods are replaced with the `useEffect` hook for achieving similar functionality. Here's how each lifecycle method corresponds to the `useEffect` hook:

1. **Mounting:**

   - **constructor:** No direct equivalent. You can use the `useState` hook to initialize state variables.
   - **componentDidMount:** You can use `useEffect` with an empty dependency array (`[]`) to mimic componentDidMount. Code inside this effect will run once after the initial render.

   Example:

   ```javascript
   import React, { useState, useEffect } from 'react';

   function MyComponent() {
       useEffect(() => {
           // Perform side effects (like data fetching) after initial render
           // This code will run once after the initial render
       }, []);

       return (
           // Component JSX
       );
   }
   ```

2. **Updating:**

   - **componentDidUpdate:** You can use `useEffect` with dependencies to mimic componentDidUpdate. Code inside this effect will run after every render if any of the dependencies have changed.

   Example:

   ```javascript
   useEffect(() => {
     // Perform side effects based on changes to specific variables (props or state)
   }, [dependency1, dependency2]);
   ```

3. **Unmounting:**

   - **componentWillUnmount:** You can return a cleanup function from the `useEffect` hook to mimic componentWillUnmount. This cleanup function will run when the component is unmounted.

   Example:

   ```javascript
   useEffect(() => {
     // Perform setup (like adding event listeners)

     // Return a cleanup function
     return () => {
       // Perform cleanup (like removing event listeners)
     };
   }, []);
   ```

React Hooks provide a more concise and readable way to handle side effects and manage component lifecycle. They also promote better code organization by separating concerns related to side effects from the component's render logic.

</details>

#### 16. What are the phases of the component lifecycle?

<details><summary><b>Answer</b></summary>

In React, the component lifecycle consists of three main phases:

1. **Mounting:**

   - This phase begins when a component is first created and inserted into the DOM.
   - It includes the following lifecycle methods:
     - `constructor`: Used for initializing state and binding event handlers.
     - `static getDerivedStateFromProps`: Used to update state based on changes in props (available in React 16 and later).
     - `render`: Responsible for rendering the component's UI based on its current props and state.
     - `componentDidMount`: Invoked immediately after the component has been rendered to the DOM. Used for performing side effects like data fetching or setting up event listeners.

2. **Updating:**

   - This phase begins when a component's props or state change and it needs to re-render.
   - It includes the following lifecycle methods:
     - `static getDerivedStateFromProps`: Similar to the mounting phase, but called before each render during updates.
     - `shouldComponentUpdate`: Allows you to control whether the component should re-render or not by returning true or false.
     - `render`: Same as in the mounting phase, responsible for rendering the component's UI.
     - `getSnapshotBeforeUpdate`: Used to capture information from the DOM before it is potentially changed (available in React 16 and later).
     - `componentDidUpdate`: Invoked immediately after updating occurs. Used for performing side effects based on changes to props or state.

3. **Unmounting:**
   - This phase begins when a component is removed from the DOM.
   - It includes the following lifecycle method:
     - `componentWillUnmount`: Invoked immediately before a component is unmounted and destroyed. Used for cleanup tasks like removing event listeners or canceling timers.

These lifecycle methods allow you to hook into specific points in a component's lifecycle and perform actions such as initialization, updating, and cleanup. However, with the introduction of React Hooks, lifecycle methods are gradually being replaced by hooks like `useEffect`, which provide a more flexible and concise way to manage side effects and component lifecycle.

</details>

#### 17. Explain the difference between componentDidMount and componentDidUpdate.

<details><summary><b>Answer</b></summary>

`componentDidMount` and `componentDidUpdate` are both lifecycle methods in React, but they serve different purposes and are called at different times during the component lifecycle.

1. **componentDidMount:**

   - This method is called immediately after a component is mounted (inserted into the DOM).
   - It is invoked only once, after the initial render.
   - Used for performing side effects that require access to the DOM, such as data fetching, setting up subscriptions, or initializing third-party libraries.
   - It is a good place to initiate asynchronous operations that need to happen once the component is ready.

2. **componentDidUpdate:**
   - This method is called immediately after an update occurs, but not for the initial render.
   - It is invoked after every update, including updates triggered by changes in props or state.
   - Used for responding to prop or state changes and performing side effects based on those changes.
   - It receives two parameters: `prevProps` and `prevState`, which contain the previous props and state values before the update.

**Key Differences:**

- `componentDidMount` is called only once after the initial render, while `componentDidUpdate` is called after every update (excluding the initial render).
- `componentDidMount` is typically used for initialization and setup tasks that need to happen once when the component is first mounted, while `componentDidUpdate` is used for responding to changes and performing side effects based on those changes.
- It's important to include proper conditions inside `componentDidUpdate` to avoid infinite loops, as updating state within this method can trigger additional renders.

In summary, `componentDidMount` is used for initial setup, while `componentDidUpdate` is used for responding to changes and updating the component in response to those changes.

</details>

## Hooks:

#### 18. What are React Hooks?

<details><summary><b>Answer</b></summary>

React Hooks are functions that allow developers to use state and other React features in functional components without writing a class. They were introduced in React 16.8 to provide a more straightforward and cleaner way to manage state and side effects in functional components.

Some key points about React Hooks include:

1. **Stateful Logic in Functional Components:** With React Hooks, functional components can now use state and other React features that were previously available only in class components. This allows for more concise and readable code.

2. **Built-in Hooks:** React provides several built-in Hooks, such as `useState`, `useEffect`, `useContext`, etc., which cover common use cases for managing state, performing side effects, and accessing context in functional components.

3. **Custom Hooks:** Developers can also create custom Hooks to encapsulate and reuse stateful logic across multiple components. Custom Hooks follow a naming convention of starting with the word "use" to denote that they are Hooks.

React Hooks have greatly simplified the development of React applications, making it easier to write and maintain functional components while still leveraging the power of React's features.

</details>

#### 19. Explain the useState Hook.

<details><summary><b>Answer</b></summary>

The `useState` Hook is a function provided by React that allows functional components to manage state. It enables functional components to have stateful logic without needing to convert them into class components. Here's how it works:

```jsx
import React, { useState } from "react";

function Example() {
  // useState returns an array with two elements:
  // 1. The current state value.
  // 2. A function to update the state.
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

In the above example, `count` is a state variable initialized with a value of `0`, and `setCount` is a function provided by the `useState` Hook to update the `count` state. When the button is clicked, the `setCount` function is called with the updated value of `count`, which triggers a re-render of the component with the new state value.

The `useState` Hook can also be used to manage more complex state, such as objects or arrays:

```jsx
import React, { useState } from "react";

function Example() {
  const [user, setUser] = useState({ name: "", age: 0 });

  return (
    <div>
      <input
        type="text"
        value={user.name}
        onChange={(e) => setUser({ ...user, name: e.target.value })}
      />
      <input
        type="number"
        value={user.age}
        onChange={(e) => setUser({ ...user, age: parseInt(e.target.value) })}
      />
      <p>
        Name: {user.name}, Age: {user.age}
      </p>
    </div>
  );
}
```

In this example, `user` is an object state variable with properties `name` and `age`. The `setUser` function is used to update the `user` state whenever the input fields change.

Overall, the `useState` Hook provides a simple and intuitive way to manage state in functional components, enabling them to have dynamic behavior and interactivity.

</details>

#### 20. What is the useEffect Hook used for?

<details><summary><b>Answer</b></summary>

The `useEffect` Hook is a function provided by React that allows functional components to perform side effects. Side effects include things like data fetching, subscriptions, or manually changing the DOM. Here's how it works:

```jsx
import React, { useState, useEffect } from "react";

function Example() {
  const [count, setCount] = useState(0);

  // useEffect is called after every render, including the first render
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

In the above example, `useEffect` is called with a function as its first argument. This function will be executed after every render, including the initial render. It's commonly used for tasks that don't require cleanup, such as updating the document title based on the component's state.

`useEffect` can also take a second argument, which is an array of dependencies. This allows you to control when the effect runs based on changes to specific values. If the array is empty, the effect runs only once after the initial render.

Here's an example of using the dependency array:

```jsx
useEffect(() => {
  // This function will only run when the count state changes
  document.title = `You clicked ${count} times`;
}, [count]);
```

Overall, the `useEffect` Hook provides a flexible way to perform side effects in functional components, allowing developers to keep their component logic organized and concise.

</details>

#### 21. How do you create a custom Hook in React?

<details><summary><b>Answer</b></summary>

Creating a custom Hook in React involves writing a JavaScript function that starts with the word "use" to denote that it's a Hook. Custom Hooks allow you to encapsulate and reuse stateful logic across multiple components. Here's how you can create a custom Hook:

```jsx
import { useState, useEffect } from "react";

function useCustomHook(initialValue) {
  const [value, setValue] = useState(initialValue);

  useEffect(() => {
    // Perform side effects or any other logic
    document.title = `Value: ${value}`;

    // Cleanup function
    return () => {
      // Cleanup logic here
    };
  }, [value]);

  // Return the value and a function to update it
  return [value, setValue];
}
```

In this example, `useCustomHook` is a custom Hook that encapsulates stateful logic. It initializes a state variable using `useState` and then uses `useEffect` to perform side effects based on changes to the state variable. The Hook returns the current value and a function to update it.

To use the custom Hook in a functional component:

```jsx
import React from "react";
import useCustomHook from "./useCustomHook";

function Example() {
  const [value, setValue] = useCustomHook(0);

  return (
    <div>
      <p>Value: {value}</p>
      <button onClick={() => setValue(value + 1)}>Increment</button>
    </div>
  );
}
```

By following this pattern, you can create reusable Hooks that encapsulate complex logic and share it across different components.

</details>

## Routing:

#### 22. How do you implement routing in React?

<details><summary><b>Answer</b></summary>

Routing in React can be implemented using various libraries, but one of the most popular libraries for this purpose is React Router. React Router provides a declarative way to render different components based on the URL.

Here's how you can implement routing in React using React Router:

1. **Install React Router:**
   You can install React Router using npm or yarn:

   ```
   npm install react-router-dom
   ```

   or

   ```
   yarn add react-router-dom
   ```

2. **Set up Routes:**
   Define the routes in your application using the `BrowserRouter` and `Route` components from React Router. Each `Route` component specifies a path and the component to render when that path matches the current URL.

   ```jsx
   import React from "react";
   import { BrowserRouter, Route } from "react-router-dom";
   import Home from "./components/Home";
   import About from "./components/About";
   import Contact from "./components/Contact";

   function App() {
     return (
       <BrowserRouter>
         <div>
           <Route exact path="/" component={Home} />
           <Route path="/about" component={About} />
           <Route path="/contact" component={Contact} />
         </div>
       </BrowserRouter>
     );
   }

   export default App;
   ```

3. **Create Components:**
   Create the components for each route. These components will be rendered when the corresponding URL is matched.

   ```jsx
   import React from "react";

   function Home() {
     return <h1>Home</h1>;
   }

   export default Home;
   ```

   ```jsx
   import React from "react";

   function About() {
     return <h1>About</h1>;
   }

   export default About;
   ```

   ```jsx
   import React from "react";

   function Contact() {
     return <h1>Contact</h1>;
   }

   export default Contact;
   ```

With these steps, you have implemented routing in your React application using React Router. Now, when users navigate to different URLs, the corresponding components will be rendered based on the routes you defined.

</details>

#### 23. What is React Router?

<details><summary><b>Answer</b></summary>

React Router is a popular library for routing in React applications. It allows developers to handle navigation and rendering different components based on the URL. React Router provides a declarative way to define routes and map them to components, enabling single-page applications (SPAs) to have multiple views without a page refresh.

Some key features of React Router include:

1. **Declarative Routing:** React Router allows you to define routes using a declarative syntax, making it easy to understand and maintain the routing logic in your application.

2. **Nested Routes:** You can nest routes within other routes, enabling complex routing configurations and hierarchical navigation structures.

3. **Route Parameters:** React Router supports route parameters, allowing you to extract dynamic segments from the URL and pass them as props to the rendered components.

4. **Programmatic Navigation:** You can navigate programmatically using the `history` object provided by React Router, enabling actions such as redirecting users after form submissions or authentication.

5. **Server-side Rendering (SSR) Support:** React Router provides support for server-side rendering, allowing your application to render routes on the server and send the initial HTML to the client for faster page loads and improved SEO.

React Router provides several components for defining routes, including `BrowserRouter`, `Route`, `Switch`, `Link`, `NavLink`, and `Redirect`. These components can be used together to create a robust routing system for your React applications.

</details>

#### 24. Explain the difference between BrowserRouter and HashRouter.

<details><summary><b>Answer</b></summary>

`BrowserRouter` and `HashRouter` are two different types of routers provided by React Router for handling routing in React applications. They differ in how they handle routing and the structure of the URLs they use.

1. **BrowserRouter:**

   - `BrowserRouter` uses the HTML5 history API to manipulate the browser's URL without causing a page refresh.
   - It uses standard URLs with paths like `/about`, `/contact`, etc.
   - `BrowserRouter` is suitable for applications deployed to servers that support URL rewriting. It's the preferred choice for applications with clean, user-friendly URLs.

   ```jsx
   import { BrowserRouter } from "react-router-dom";

   function App() {
     return <BrowserRouter>{/* Routes and components */}</BrowserRouter>;
   }
   ```

2. **HashRouter:**

   - `HashRouter` uses the hash portion of the URL (the part after `#`) to simulate different pages or states within a single HTML page.
   - It appends a hash fragment to the URL, resulting in URLs like `/#/about`, `/#/contact`, etc.
   - `HashRouter` is suitable for applications deployed to environments that do not support URL rewriting, such as GitHub Pages or static file servers. It ensures that the routing works even when the user manually types or bookmarks URLs.

   ```jsx
   import { HashRouter } from "react-router-dom";

   function App() {
     return <HashRouter>{/* Routes and components */}</HashRouter>;
   }
   ```

In summary, the main difference between `BrowserRouter` and `HashRouter` lies in how they manipulate the browser's URL and the structure of the URLs they produce. `BrowserRouter` uses clean URLs, while `HashRouter` uses URLs with a hash fragment. Choose the appropriate router based on your deployment environment and the desired URL structure for your application.

</details>

## Forms:

#### 25. How do you handle forms in React?

<details><summary><b>Answer</b></summary>

Handling forms in React involves using state to track the values of form inputs and event handlers to update the state when the user interacts with the form. Here's a basic example of how you can handle forms in React:

```jsx
import React, { useState } from "react";

function FormExample() {
  // Define state variables for form inputs
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  // Event handler to update the name state
  const handleNameChange = (event) => {
    setName(event.target.value);
  };

  // Event handler to update the email state
  const handleEmailChange = (event) => {
    setEmail(event.target.value);
  };

  // Event handler to submit the form
  const handleSubmit = (event) => {
    event.preventDefault();
    // Do something with the form data (e.g., submit to a server)
    console.log("Name:", name);
    console.log("Email:", email);
  };

  return (
    <form onSubmit={handleSubmit}>
      <div>
        <label htmlFor="name">Name:</label>
        <input type="text" id="name" value={name} onChange={handleNameChange} />
      </div>
      <div>
        <label htmlFor="email">Email:</label>
        <input
          type="email"
          id="email"
          value={email}
          onChange={handleEmailChange}
        />
      </div>
      <button type="submit">Submit</button>
    </form>
  );
}

export default FormExample;
```

In this example:

- State variables `name` and `email` are initialized using the `useState` Hook to track the values of the form inputs.
- Event handlers `handleNameChange` and `handleEmailChange` update the state variables when the user types in the input fields.
- The `handleSubmit` event handler is called when the form is submitted. It prevents the default form submission behavior, logs the form data to the console, and can be extended to perform other actions such as submitting the form to a server.

This pattern allows you to create controlled forms in React, where form inputs are controlled by React state. Controlled forms provide a single source of truth for the form data, making it easier to manage and validate.

</details>

#### 26. Explain controlled vs. uncontrolled components in React forms.

<details><summary><b>Answer</b></summary>

**Controlled Components:**

- In controlled components, form data is handled by React state.
- The value of form elements like input fields, textarea, and select elements are controlled by React state variables.
- Changes to the form elements are handled through event handlers that update the state.
- The form elements always reflect the current state, and any user input is immediately reflected in the state.

```jsx
import React, { useState } from "react";

function ControlledForm() {
  const [name, setName] = useState("");

  const handleChange = (event) => {
    setName(event.target.value);
  };

  return (
    <form>
      <input type="text" value={name} onChange={handleChange} />
      <p>Name: {name}</p>
    </form>
  );
}
```

**Uncontrolled Components:**

- In uncontrolled components, form data is handled by the DOM.
- The value of form elements is managed by the DOM itself, and React does not control it.
- Refs are typically used to access the DOM elements to read their values when needed, such as when the form is submitted.

```jsx
import React, { useRef } from "react";

function UncontrolledForm() {
  const inputRef = useRef(null);

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log("Name:", inputRef.current.value);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" ref={inputRef} />
      <button type="submit">Submit</button>
    </form>
  );
}
```

**Key Differences:**

- **Controlled Components:** Provide a single source of truth for form data, making it easier to manage and validate form inputs. Suitable for forms with dynamic behavior and validation requirements.
- **Uncontrolled Components:** Allow direct access to DOM elements, useful for integrating with third-party libraries or working with legacy code. Less common in modern React applications but still have their use cases.

In general, controlled components are the preferred approach for handling forms in React because they provide more control and predictability over form data.

</details>

#### 27. What is Formik and how does it simplify form handling in React?

<details><summary><b>Answer</b></summary>

**Formik** is a popular form management library for React that simplifies the process of building and managing forms. It provides a set of tools and utilities to handle common form tasks such as validation, error handling, and form submission.

**Key Features of Formik:**

1. **Declarative Form Handling:** Formik allows you to define your form using a declarative approach, making it easy to specify form fields, validation rules, and submission logic.

2. **Form State Management:** Formik manages the state of your form internally, including form values, errors, touched fields, and submission status. This eliminates the need to manually track form state using React state variables.

3. **Validation Support:** Formik provides built-in support for form validation, allowing you to define validation rules for each form field. It supports synchronous and asynchronous validation, as well as validation based on field dependencies.

4. **Error Handling:** Formik automatically handles error messages and validation feedback, making it easy to display error messages next to the corresponding form fields.

5. **Form Submission:** Formik simplifies form submission by providing utilities to handle form submission events and manage submission status. It supports asynchronous form submission and provides hooks for integrating with external APIs.

6. **Integration with Yup:** Formik seamlessly integrates with Yup, a schema validation library, allowing you to define complex validation schemas and use them with your Formik forms.

Here's a basic example of how you can use Formik to handle a simple form:

```jsx
import React from "react";
import { Formik, Form, Field, ErrorMessage } from "formik";

function MyForm() {
  return (
    <Formik
      initialValues={{ email: "", password: "" }}
      onSubmit={(values, actions) => {
        console.log("Form submitted:", values);
        actions.setSubmitting(false);
      }}
      validate={(values) => {
        const errors = {};
        if (!values.email) {
          errors.email = "Email is required";
        }
        if (!values.password) {
          errors.password = "Password is required";
        }
        return errors;
      }}
    >
      {({ isSubmitting }) => (
        <Form>
          <Field type="email" name="email" />
          <ErrorMessage name="email" component="div" />
          <Field type="password" name="password" />
          <ErrorMessage name="password" component="div" />
          <button type="submit" disabled={isSubmitting}>
            Submit
          </button>
        </Form>
      )}
    </Formik>
  );
}

export default MyForm;
```

In this example, `Formik`, `Form`, `Field`, and `ErrorMessage` components are imported from Formik library to build the form. `Formik` component wraps the form and manages its state and submission, while `Field` components represent form inputs. `ErrorMessage` components display validation errors for each field.

Formik simplifies the process of building and managing forms in React by providing a comprehensive set of tools and utilities, reducing boilerplate code and making form handling more efficient and maintainable.

</details>

## Redux:

#### 28. What is Redux?

<details><summary><b>Answer</b></summary>

**Redux** is a predictable state container for JavaScript applications, primarily used with React or any other view library/framework. It provides a centralized store for managing the state of your entire application, making it easier to manage and update state in a predictable and scalable way.

**Key Concepts of Redux:**

1. **Store:** Redux stores the state of your application in a single JavaScript object called the store. The store holds the entire state tree of your application and can be accessed and updated using actions.

2. **Actions:** Actions are plain JavaScript objects that represent changes to the state of your application. They are dispatched to the Redux store using the `dispatch` function. Actions must have a `type` property indicating the type of action being performed.

3. **Reducers:** Reducers are pure functions that specify how the application's state changes in response to actions. Reducers take the current state and an action as arguments and return a new state based on the action type.

4. **Store Updates:** When an action is dispatched, Redux passes the current state and the action to the root reducer, which returns the new state. The store then updates its state with the new state returned by the reducer.

5. **Single Source of Truth:** Redux promotes a single source of truth for your application's state, making it easier to reason about and debug your application. All state changes are centralized in the store, which helps prevent inconsistencies and data duplication.

6. **Immutable State:** Redux state is immutable, meaning that the state cannot be changed directly. Instead, reducers return a new state object with updated values whenever a change is needed.

Redux is commonly used in conjunction with React to manage the state of React applications, but it can also be used with other JavaScript frameworks or libraries. It provides a predictable and efficient way to manage state in complex applications, helping developers write more maintainable and scalable code.

</details>

#### 29. Explain the core principles of Redux.

<details><summary><b>Answer</b></summary>

**Redux** is built around three core principles that guide its design and usage:

1. **Single Source of Truth:**
   Redux maintains the entire state of your application in a single JavaScript object called the store. This creates a single source of truth for your application's state, making it easier to reason about and manage state changes. Having a centralized store also simplifies debugging and ensures consistency across your application.

2. **State is Read-Only and Immutable:**
   In Redux, state is immutable, meaning that it cannot be changed directly. Instead, state changes are made by dispatching actions to the Redux store. Reducers then handle these actions and return a new state object with updated values. By enforcing immutability, Redux ensures that state changes are predictable and traceable, helping to prevent bugs and side effects.

3. **Changes are Made with Pure Functions:**
   Redux uses pure functions called reducers to specify how the application's state changes in response to actions. Reducers take the current state and an action as arguments, and return a new state object based on the action type. Because reducers are pure functions with no side effects, they are easy to test and reason about. They also ensure that state changes are predictable and consistent, making your application more reliable and maintainable.

By adhering to these core principles, Redux provides a predictable and efficient way to manage state in complex applications. It promotes a unidirectional data flow, where state changes are triggered by actions and handled by reducers, leading to more maintainable, scalable, and bug-free code.

</details>

#### 30. What are the three parts of a Redux application?

<details><summary><b>Answer</b></summary>

A Redux application consists of three main parts:

1. **Store:**
   The store is a JavaScript object that holds the entire state tree of your application. It is the central hub of a Redux application, responsible for managing and updating the application's state. The store is created using the `createStore` function provided by Redux, and it exposes methods such as `getState`, `dispatch`, and `subscribe` to interact with the state.

2. **Actions:**
   Actions are plain JavaScript objects that represent changes to the state of your application. They are the only way to send data to the Redux store. Actions must have a `type` property that describes the type of action being performed, and they can optionally include additional data (payload) needed to update the state. Actions are created using action creator functions and dispatched to the Redux store using the `dispatch` function.

3. **Reducers:**
   Reducers are pure functions that specify how the application's state changes in response to actions. They take the current state and an action as arguments, and return a new state object based on the action type. Reducers should be pure functions with no side effects, meaning that they should not modify the original state object or perform any asynchronous operations. Redux provides the `combineReducers` function to combine multiple reducers into a single root reducer.

Together, these three parts form the core architecture of a Redux application. Actions represent what happened, reducers specify how the state changes, and the store holds the single source of truth for the application's state. By following the principles of Redux, developers can build scalable, predictable, and maintainable applications with clear data flow and state management.

</details>

#### 31. How do you connect React components to Redux?

<details><summary><b>Answer</b></summary>

To connect React components to Redux, you can use the `connect` function provided by the `react-redux` library. This function creates a higher-order component (HOC) that wraps your component and connects it to the Redux store. Here's how you can connect a React component to Redux:

1. **Install react-redux:**
   First, you need to install the `react-redux` library using npm or yarn:

   ```
   npm install react-redux
   ```

   or

   ```
   yarn add react-redux
   ```

2. **Create a Container Component:**
   Create a container component that will serve as the connected version of your original component. This container component will use the `connect` function to connect to the Redux store and pass state and actions as props to your component.

   ```jsx
   import { connect } from "react-redux";
   import MyComponent from "./MyComponent";

   // Map state from Redux store to component props
   const mapStateToProps = (state) => ({
     data: state.data,
   });

   // Map actions to component props
   const mapDispatchToProps = {
     fetchData,
   };

   // Connect component to Redux store
   const ConnectedComponent = connect(
     mapStateToProps,
     mapDispatchToProps
   )(MyComponent);

   export default ConnectedComponent;
   ```

3. **Access Redux State and Dispatch Actions:**
   Inside your original component (`MyComponent`), you can now access Redux state and dispatch actions as props passed by the container component.

   ```jsx
   import React from "react";

   function MyComponent(props) {
     const { data, fetchData } = props;

     return (
       <div>
         <p>Data: {data}</p>
         <button onClick={fetchData}>Fetch Data</button>
       </div>
     );
   }

   export default MyComponent;
   ```

By following these steps, you can connect your React components to the Redux store and access Redux state and dispatch actions within your components. This allows you to manage state and perform actions in Redux while keeping your components decoupled from the Redux implementation details.

</details>

## Context API:

#### 32. What is the Context API in React?

<details><summary><b>Answer</b></summary>

The Context API is a feature introduced in React 16.3 that provides a way to share data between components without having to pass props manually through each level of the component tree. It allows you to create global data that can be accessed by any component in the component tree, regardless of how deeply nested they are.

The Context API consists of two main parts:

1. **Context Object:**
   A context object is created using the `createContext` function provided by React. This context object represents the shared data that you want to make available to your components. It typically contains a `Provider` component and a `Consumer` component.

2. **Provider Component:**
   The `Provider` component is used to wrap the part of your component tree where you want to make the context data available. It accepts a `value` prop that specifies the data to be shared. Any component within the `Provider`'s subtree can access this data using the `Consumer` component or the `useContext` Hook.

Here's a basic example of how you can use the Context API in React:

```jsx
import React, { createContext, useContext } from "react";

// Create a context object
const MyContext = createContext();

// Create a provider component
function MyProvider({ children }) {
  const sharedData = "Hello from Context";

  return <MyContext.Provider value={sharedData}>{children}</MyContext.Provider>;
}

// Create a consumer component
function MyConsumer() {
  const sharedData = useContext(MyContext);
  return <p>{sharedData}</p>;
}

// Example usage
function App() {
  return (
    <MyProvider>
      <div>
        <h1>App</h1>
        <MyConsumer />
      </div>
    </MyProvider>
  );
}

export default App;
```

In this example, the `MyProvider` component wraps the `MyConsumer` component, making the `sharedData` available to it. The `MyConsumer` component accesses the shared data using the `useContext` Hook.

The Context API is particularly useful for sharing global data such as themes, user authentication, localization, or any other data that needs to be accessed by multiple components in your application.

</details>

#### 33. How do you use the useContext Hook?

<details><summary><b>Answer</b></summary>

The `useContext` Hook is used to consume values from a React context within a functional component. It allows you to access context values without using a `Consumer` component.

Here's how you can use the `useContext` Hook:

1. **Import the `useContext` Hook:**
   First, you need to import the `useContext` Hook from the React library.

   ```jsx
   import React, { useContext } from "react";
   ```

2. **Access the Context Value:**
   Call the `useContext` Hook with the context object that you want to consume. This Hook returns the current context value provided by the nearest `Provider` component in the component tree.

   ```jsx
   const contextValue = useContext(MyContext);
   ```

   Replace `MyContext` with the context object that you created using `createContext`.

Here's an example of how you can use the `useContext` Hook:

```jsx
import React, { createContext, useContext } from "react";

// Create a context object
const MyContext = createContext();

// Provider component
function MyProvider({ children }) {
  const sharedData = "Hello from Context";
  return <MyContext.Provider value={sharedData}>{children}</MyContext.Provider>;
}

// Consumer component
function MyConsumer() {
  const sharedData = useContext(MyContext);
  return <p>{sharedData}</p>;
}

// Example usage
function App() {
  return (
    <MyProvider>
      <div>
        <h1>App</h1>
        <MyConsumer />
      </div>
    </MyProvider>
  );
}

export default App;
```

In this example, the `MyConsumer` component uses the `useContext` Hook to access the value provided by the `MyContext.Provider` component. It retrieves the shared data (`sharedData`) and renders it inside a paragraph (`<p>`) element.

</details>

#### 34. When would you use Context API instead of prop drilling?

<details><summary><b>Answer</b></summary>

The decision to use the Context API instead of prop drilling depends on the complexity of your application and the level of nesting at which the shared data is needed. Here are some scenarios where using the Context API might be more appropriate:

1. **Deeply Nested Components:**
   If you have deeply nested components that need access to shared data, prop drilling can become cumbersome and lead to prop clutter in intermediate components. In such cases, using the Context API can simplify the data flow by providing a centralized way to share data across the component tree without passing props manually through each level.

2. **Global or Theme Data:**
   If you have global data or theme settings that need to be accessed by multiple components throughout your application, prop drilling can be impractical. Instead, using the Context API allows you to create a global context that provides access to this data from any component in your application without explicitly passing props down the component tree.

3. **Cross-Cutting Concerns:**
   Certain concerns, such as user authentication, localization, or theming, are cross-cutting and affect multiple parts of your application. Using the Context API to manage these concerns allows you to encapsulate the related logic in a single place and provide access to it wherever needed, without coupling components to each other through props.

4. **Dynamic Data or Configuration:**
   If the data or configuration that needs to be shared is dynamic and may change over time, using the Context API provides a convenient way to propagate updates to all components that depend on that data. With prop drilling, you would need to manually pass updated props down the component tree whenever the data changes.

In summary, the Context API is a powerful tool for managing shared data and cross-cutting concerns in React applications, particularly in scenarios where prop drilling becomes cumbersome or impractical due to the depth or complexity of the component tree.

</details>

#### 35. The major difference between Context API and Redux?

<details><summary><b>Answer</b></summary>

**Context API:**

- Context API is a feature provided by React for managing global state within a React application.
- It is built into React and does not require any additional libraries.
- Context API is primarily used for small to medium-sized applications or for managing local state within a component tree.
- Context API provides a way to pass data through the component tree without having to pass props manually at every level.

**Redux:**

- Redux is a separate library (not part of React) for managing global state in JavaScript applications, commonly used with React.
- Redux provides a centralized store to manage the state of your entire application.
- It is designed for managing large-scale applications with complex state management needs, such as handling asynchronous actions, middleware integration, and time-travel debugging.
- Redux follows a strict unidirectional data flow, where state changes are triggered by actions and handled by reducers.

**Major Differences:**

1. **Scope and Complexity:**

   - Context API is built into React and is primarily used for managing local state within a component tree or sharing data between closely related components.
   - Redux is a separate library with a larger scope, designed for managing global state and handling complex state management scenarios in large-scale applications.

2. **Use Cases:**

   - Context API is suitable for managing small to medium-sized applications or for managing local state within a component tree.
   - Redux is preferred for managing large-scale applications with complex state management needs, such as applications with multiple views, data fetching, and complex data dependencies.

3. **Learning Curve:**

   - Context API is simpler and has a lower learning curve compared to Redux, making it easier to get started with for beginners or for simpler use cases.
   - Redux has a steeper learning curve due to its strict architecture and additional concepts such as actions, reducers, and middleware.

4. **Integration with React Ecosystem:**
   - Context API integrates seamlessly with React and is a part of the official React library.
   - Redux requires additional setup and integration with React using the `react-redux` library, although it provides additional features and capabilities for managing state.

In summary, while both Context API and Redux are used for managing state in React applications, they differ in scope, complexity, and use cases. Context API is simpler and more lightweight, suitable for smaller applications or local state management, while Redux is designed for larger-scale applications with complex state management needs.

</details>
