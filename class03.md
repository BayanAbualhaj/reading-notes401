# reading notes

##  Express REST API


### 3 cases to use middleware
1. Use Custom Middleware to Detect and Fix 404s in ASP.NET Core Apps
2. Middleware can add HTTP headers, add internal flags for use by your business logic, etc. 
3. looking up a session token in Redis, or performing a GeoIP lookup from a MaxMind dataset.

___________________________

### True or false: The route handler is middleware?

false but they are too semiler to each other but he way you program Express, the distinction is pretty blurry.

In Express, there is no hard and fast distinction between the two. Someone would generally call something middleware that examines a bunch of different requests and usually prepares the request for further processing. Someone would generally call something a route handler that is targeted at a specific URL (or type of URL) and whose main purpose is to send a response back to the client for that URL.

* For more information you can visit this web site :
[ Middleware vs route handler ](https://stackoverflow.com/questions/58925276/what-is-the-difference-between-a-route-handler-and-middleware-function-in-expres)

__________________________

### Ways can a middleware function end the process and send data to the browser
* This way you can ensure the request object in middleware receiving data contains an attribute containing data passed by outer middleware.

* Middleware gives you access to req and res objects in the app’s request-> response cycle.

* Execute any code.
* Make changes to the request and the response objects.
* End the request-response cycle.
* Call the next middleware in the stack using next()

Middleware is a great tool to organize your code to work in the request-response cycle. It is basically a function that has access to the req and res objects of your application. It can be thought of as a series of tasks that the developer performs before the request is handled by the application. You can code your own middleware functions or use built-in or 3rd party functions.

* For more information you can visit this web site :
[Middleware](https://afteracademy.com/blog/expressjs-middleware-in-javascript)

__________________________

### At what point in the request lifecycle can you “inject” middleware?

* in the routing, how come?
    - The router will dispatch the request to a route or controller, as well as run any route specific middleware.
    - If the request passes through all of the matched route's assigned middleware, the route or controller method will be executed and the response returned by the route or controller method will be sent back through the route's chain of middleware.


_____________________________

### What can cause express to error with “Request headers sent twice, cannot start a second response”


* Cannot set headers after they are sent to the client: This error happens because the code ran methods that set response headers more than once in the same handler

* Cannot set headers : Express states you should delegate the error handling to the default Express handlers. It will send an error and close the connection for you.

* For more information you can visit this web site :
[express errors](https://zellwk.com/blog/express-errors/)

_____________________________________

## What is?

* **Middleware** is software that lies between an operating system and the applications running on it. Essentially functioning as hidden translation layer, middleware enables communication and data management for distributed applications.

* **The request object** allows you to submit a POST or GET request to an URL. Essentially it provides a way to make REST API requests to another URL.You can also send HEAD, PUT, DELETE, OPTIONS and PATCH requests.

* [**The res object**](https://www.tutorialspoint.com/nodejs/nodejs_response_object.htm) represents the HTTP response that an Express app sends when it gets an HTTP request. 

* **application middleware**:
    - Application Programming Interfaces (APIs)
        Many middleware services are accessed through APIs, which are sets of tools, definitions, and protocols that allow applications to communicate with each other. APIs make it possible to connect completely different products and services through a common layer.
    - New application development
        Middleware can support modern and popular runtimes for a variety of use cases. Developers and architects can work with agility across platforms, following sets of foundational runtimes, frameworks, and programming languages. Middleware can also deliver commonly used functions such as web servers, single sign-on (SSO), messaging, and in-memory caching.


* **The routing*** has been implemented as middleware. We are still using FastRoute as the default router but it is not tightly coupled to it. If you wanted to implement another routing library you could by creating your own implementations of the routing interfaces.

* **Test Driven Development (TDD)** is software development approach in which test cases are developed to specify and validate what the code will do. In simple terms, test cases for each functionality are created and tested first and if the test fails then the new code is written in order to pass the test and making code simple and bug-free.

* **Behavioural Testing** is a testing of the external behaviour of the program, also known as black box testing. It is usually a functional testing.
