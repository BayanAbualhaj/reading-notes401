# Reading Notes 

## Component Based UI

### Name 5 Javascript UI Frameworks (other than React):
1. Vue
2. Angular
3. Ember
4. Backbone.js
5. Meteor


_________________________________

### What’s the difference between a framework and a library?

![](https://miro.medium.com/max/800/1*tMJUTqe2dKlueiNU17IZug.png)

The technical difference between a framework and library lies in a term called inversion of control. When you use a library, you are in charge of the application flow. You choose when and where to call the library. When you use a framework, the framework is in charge of the flow. It provides you with a few places to plug in your code, but it calls the code you plugged in as needed.

frameworks are more opinionated and libraries are more flexible. 

____________________________________

* ***state*** of a program is defined as its condition regarding stored inputs. The term "state" here is used similarly to how it is used in science — whereas the state of an object, for instance, as a gas, liquid or solid, shows its current physical makeup, the state of a computer program shows its current values or contents.

* **Templates** are a feature programming language that allows functions and classes to operate with generic types. This allows a function or class to work on many different data types without being rewritten for each one.

* **Rendering** or image synthesis is the process of generating a photorealistic or non-photorealistic image from a 2D or 3D model by means of a computer program. The resulting image is referred to as the render. Multiple models can be defined in a scene file containing objects in a strictly defined language or data structure.

_________________________________

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR6VGH2PVcG6xAr4Q5Aukpzb-UbyMHwYM1ZPQ&usqp=CAU)


- **ReactDOM.render** this one I noticed in code Pen it only render one element inside it. and it take 2 params one for the element and the other of the parent element.

- Introducing JSX
    * JSX it is a syntax extension to JavaScript.
    * produces React “elements”.
    * React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. 
    * JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.
    * You may use quotes to specify string literals as attributes
    * You may also use curly braces to embed a JavaScript expression in an attribute.
    * Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute.
    * You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.
    * If a tag is empty, you may close it immediately with />, like XML:the img tag
    * JSX tags may contain children:like the div tag can contain more than one child.
    * It is safe to embed user input in JSX
    * React.createElement(): performs a few checks to help you write bug-free code but essentially it creates an object.
    * 
- Rendering Elements:
    * most React apps only call ReactDOM.render() once. In the next sections we will learn how such code gets encapsulated into stateful components.
    * React Only Updates What’s Necessary
    * thinking about how the UI should look at any given moment, rather than how to change it over time, eliminates a whole class of bugs.