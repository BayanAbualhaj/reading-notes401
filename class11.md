# Reading Notes

### Why is access control important?
Access control is a fundamental component of security compliance programs that ensures security technology and access control policies are in place to protect confidential information, such as customer data. Most organizations have infrastructure and procedures that limit access to networks, computer systems, applications, files and sensitive data, such as personally identifiable information (PII) and intellectual property.
_________________________
### Describe an application that would need access control.

* apps in  Most organizations have infrastructure and procedures that limit access to networks, computer systems, applications, files and sensitive data, such as personally identifiable information (PII) and intellectual property. so all need control access.
____________________________________
### What is a role used for?
### Why is role based access control more scalable than discretionary or mandatory access control?

* **Role-based access control (RBAC)**. This is a widely used access control mechanism that restricts access to computer resources based on individuals or groups with defined business functions -- e.g., executive level, engineer level 1, etc. -- rather than the identities of individual users. The role-based security model relies on a complex structure of role assignments, role authorizations and role permissions developed using role engineering to regulate employee access to systems. RBAC systems can be used to enforce MAC and DAC frameworks.
_______________________________

* **Authorization** is a security mechanism used to determine user/client privileges or access levels related to system resources, including computer programs, files, services, data and application features. 

* T[he object-capability model](https://en.wikipedia.org/wiki/Object-capability_model) : is a computer security model. A capability describes a transferable right to perform one (or more) operations on a given object.
____________________________

### events node.js

![ev](https://i.stack.imgur.com/BTm1H.png)

* Event-Driven Programming is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision. 

* Event-Driven Programming makes use of the following concepts:

    1. An Event Handler is a callback function that will be called when an event is triggered.
    2. A Main Loop listens for event triggers and calls the associated event handler for that event.

* EventEmitter:Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Programming in our project right away. 

* Removing Listeners
There will likely come a time when you want to remove an event listener from an event. This could be for performance reasons (the event is no longer needed) or to avoid memory leaks (if an event listener references an object that is no longer needed, it won’t be able to be garbage-collected. This can lead to a build up of unnecessary objects).


### Object Oriented Programming + Event-Driven Programming

* hese two make for a very valuable combination in a wide variety of situations
* The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.
* we can make use of Event-driven programming. By registering event listeners we can actually reverse the flow of communication between our objects.


