# React Components

- React applications are made out of components.

## What’s a component?

- A component is a small, reusable chunk of code that is responsible for one job. That job is often to render some HTML.

```
import React from 'react'; 
// creates an object named React which contains methods necessary to use the React library.
import ReactDOM from 'react-dom';
// The methods imported from 'react-dom' are meant for interacting with the DOM.
 
class ComponentClass extends React.Component {
// take a component class to make reusable blocks of code 
// React.Component is a JavaScript class
// syntax class YourComponentNameGoesHere extends React.Component {}.

  render() {
    return <h1>Hello world</h1>;
    //A render method is a property whose name is render, and whose value is a function. The term “render method” can refer to the entire property, or to just the function part.
  }
};
 
ReactDOM.render(
  <ComponentClass />,
  document.getElementById('app')
);

```
