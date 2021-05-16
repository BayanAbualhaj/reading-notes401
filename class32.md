# Custom Hooks

![](https://miro.medium.com/max/3280/1*uZ8WSki-46Kkls1TefrLIQ.jpeg)

## What does a component’s lifecycle refer to?

Components are created (mounted on the DOM), grow by updating, and then die (unmount on DOM).

_____________

## Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

to use async and await

________________

## Why are functional components preferred over class components?

* Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks.
* It has less code which makes it more readable.

_______________

## What is wrong with the following code?

for loop affect the useEffect
________________________

## Terms 

1. **reducer hook**: use sometimes to manage the state of the application. It is very similar to the useState hook, just more complex.

2. **effect hook**:The Effect Hook lets you perform side effects in function components.

3. **state hook**: special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components.

____________________

* A custom Hook is a normal function but we hold them to a different standard. By adding the word use to the beginning, it lets us know that this function follows the rules of Hooks.

* Five Important Rules for Hooks:

    1. Never call Hooks from inside a loop, condition or nested function
    2. Hooks should sit at the top-level of your component
    3. Only call Hooks from React functional components
    4. Never call a Hook from a regular function
    5. Hooks can call other Hooks

* The Benefits of Using Hooks:

Hooks have a lot of benefit to us as developers, and they are going to change the way we write components for the better.

* **useToggle**:what this hook does is that, it takes a parameter with value true or false and toggles that value to opposite. It's useful when we want to take some action into it's opposite action.

* **useReducer** is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.
