# Context API

![](https://www.qed42.com/sites/default/files/2020-05/Context%20API%20in%20React%20with%20Hooks.png)

## Describe use cases for useMemo() and useReducer().

1. useMemo() it allows you to apply memoization to any value type (not just functions).

2. useReducer() to use in order to reset the calculator to a default state of zero when clearing it out.

_____________________

## Why do custom hooks need the use prefix?

so react can know it’s custom hook.

____________________

## What do custom hooks usually do?

We can decide what it takes as arguments, and what, if anything, it should return. In other words, it’s just like a normal function.

____________________

## Using any list of custom hooks, research and name one that you think will be useful in your applications 

useToggle: change a value between true and false.used for show and hide modal, show more/show less text, open/close side menu.

__________________

## Describe how a hook that fetches API data might work

use the useEffect and useState Hooks to fetch and display information in a sample application, using JSON server (Links to an external site.) as a local API for testing purposes. You’ll load information when a component first mounts and save customer inputs with an API

_________________________________

* **reducer**:reducer	is a function that determines changes to an application’s state. It uses the action it receives to determine this change.

_______________________________


* **Context**:is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.

* **Before You Use Context** :Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult.

* If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

* Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

* The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.
