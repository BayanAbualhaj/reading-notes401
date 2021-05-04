# Routing

## Do child components have direct access to props/state from the parent?

Not in a dirict way 

_______________________

## When a component “wraps” another component, how does the child component’s output get rendered?

By add the component as a children props

___________________

## Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?

Yes we can implement child in it.

_______________________

## What trick can a parent use to share all props with it’s children

1. React.Children to loop over the children 
2. React.cloneElement clone the element with new props.
______________________

# Terms:
* **props.children** allows us to compose components, and therefore our front-end interface as a consequence; harnessing the real power of the React component model.

* **Composition** is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop.

_______________________
## React Router

![](https://miro.medium.com/max/1200/1*TKvlTeNqtkp1s-eVB5Hrvg@2x.png)

* React Router has been broken into three packages: 

1. react-router
2. react-router-dom
3. react-router-native.

*  there are BrowserRouter and HashRouter components.

* BrowserRouter should be used when you have a server that will handle dynamic requests.

* HashRouter should be used for static websites.

* Router components only expect to receive a single child element. 

* The <Route> component is the main building block of React Router. Anywhere that you want to only render content based on the location’s pathname, you should use a <Route> element.

* Routes can be created anywhere inside of the router, but often it makes sense to render them in the same place

* What does the <Route> render?
    1. component :A React component.
    2. render — A function that returns a React element
    3. children — A function that returns a React element. 

* component or render prop should be used.

___________________________

## About Queries

* **Types of Queries**:

    1. Single Elements
        - getBy...: Returns the matching node for a query, and throw a descriptive error if no elements match or if more than one match is found (use getAllBy instead if more than one element is expected).
        - queryBy...: Returns the matching node for a query, and return null if no elements match. This is useful for asserting an element that is not present. Throws an error if more than one match is found (use queryAllBy instead if this is OK).
        - findBy...: Returns a Promise which resolves when an element is found which matches the given query. The promise is rejected if no element is found or if more than one element is found after a default timeout of 1000ms. If you need to find more than one element, use findAllBy.

    2. Multiple Elements:
        - getAllBy...: Returns an array of all matching nodes for a query, and throws an error if no elements match.
        - queryAllBy...: Returns an array of all matching nodes for a query, and return an empty array ([]) if no elements match.
        - findAllBy...: Returns a promise which resolves to an array of elements when any elements are found which match the given query. The promise is rejected if no elements are found after a default timeout of 1000ms.

* **Priority** 
    1. Queries Accessible to Everyone
    2. Semantic Queries 
    

________________________



