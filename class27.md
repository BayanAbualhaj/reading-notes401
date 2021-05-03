# Props and State

### Does a deployed React application require a server?

You don’t necessarily need a static server in order to run a Create React App project in production.

-----

### Why do we prefer to test a React application at the behavior rather than the unit level?

Testing components that are not purely functional and are responsible for behavior isn’t difficult, but there aren’t as many resources on the web that describe how to do this.

_____

### What does npm run build do?

npm run build does nothing unless you specify what “build” does in your package.
______________________


### Describe the actual composition / architecture of a React application

React.js is not strict to an architecture pattern. It is just a view that caters to the user interface.

_________________________

* **Behaviour Driven Development (BDD)** is a synthesis and refinement of practices stemming from Test Driven Development (TDD) and Acceptance Test Driven Development (ATDD).

* **Acceptance testing** is a term used in agile software development methodologies, particularly extreme programming, referring to the functional testing of a user story by the software development team during the implementation phase.

* **Mounting** is a process by which the operating system makes files and directories on a storage device (such as hard drive, CD-ROM, or network share) available for users to access via the computer's file system.

*  **build** is a pre-release version and as such is identified by a build number, rather than by a release number

_______________________________

#### setState

**setState()** is the only legitimate way to update state after the initial state setup. Let’s say we have a search component and want to display the search term a user submits.

![](https://i1.wp.com/css-tricks.com/wp-content/uploads/2018/04/image_preview-1.jpeg?w=300&ssl=1)




#### Handling Events

**Handling events** with React elements is very similar to handling events on DOM elements. There are some syntax differences:

1. React events are named using camelCase, rather than lowercase.
2. With JSX you pass a function as the event handler, rather than a string.

![](https://miro.medium.com/max/600/0*qerRB89neIaZKoqD.png)


#### Forms

* We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.


#### State and Lifecycle

![](https://cdn-media-1.freecodecamp.org/images/1*_drMYY_IEgboMS4RhvC-lQ.png)

* You can convert a function component like Clock to a class in five steps:

    - Create an ES6 class, with the same name, that extends React.Component.
    - Add a single empty method to it called render().
    - Move the body of the function into the render() method.
    - Replace props with this.props in the render() body.
    - Delete the remaining empty function declaration.

* Adding Lifecycle Methods to a Class
In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.

* We want to set up a timer whenever the Clock is rendered to the DOM for the first time. This is called “mounting” in React.

* We also want to clear that timer whenever the DOM produced by the Clock is removed. This is called “unmounting” in React.

* We can declare special methods on the component class to run some code when a component mounts and unmounts

#### Components and Props

![](https://www.techdiagonal.com/wp-content/uploads/2019/09/react-props-blog-image-design-2.jpg)

* Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

