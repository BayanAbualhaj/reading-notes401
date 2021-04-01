# Reading-Notes 

## What does Singleton mean?

* A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object. This is helpful usually when a single object is required to coordinate actions across a system.

* The singleton pattern is used in programming languages to define a global variable. A single object used across systems remains constant and needs to be defined only once rather than many times.

_____________________________

## ow the Singleton pattern can be used with Node modules, specifically with classes

* The singleton class can be extended by inheritance, and clients must be able to use extended classes without making any changes to it.

![heros](https://miro.medium.com/max/706/0*i9gq7LvJvVXkUz7o.jpeg)

* Both Batman and Spiderman have implemented the singleton pattern in their construction and store a reference to the only object of each class (our hero!). These classes are as follows:

![123](https://miro.medium.com/max/875/0*9rHSpItIWgGFV-bC.png)

![321](https://miro.medium.com/max/875/0*aBUsJtTXPRqw6nK2.png)

* Finally, the sample code for this interaction is as follows:

![456](https://miro.medium.com/max/875/0*eLesW_PP2OzKhjkK.png)

* The result obtained is shown in the following image:
![654](https://miro.medium.com/max/875/0*4kRoGbVfnSgdxEy8.png)

- then run npm script that run the singleton pattern.

____________________________________

## If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

1. define a function with the three lifecycle methods as arguments:
    - req
    - res
    - next

2. Using the req Object: To identify the currently logged in user, you can construct a custom middleware that can fetch the user through authentication steps.

3. Applying the res Object: method will apply Success, on each function call.

4. The next() method will tell Express.js to move on to following middleware once the execution completes.

5. Ending the Request and Response Cycle : Express.js also allows you to end the request and response cycle in your custom middleware. A common use case for a custom middleware is to validate a user’s data set on your req object. How ?
    - If the user’s data exists in the req object, your custom middleware will move on to following functions. 
    -  If a particular user’s data is not in the object, the .send() method on the res object will forward the error status code 401 and a message to the client side.

_____________________________________

## What is in JavaScript?

![789](https://elantechlab.com/wp-content/uploads/2021/03/download-4.jpeg)


1. **[Router Middleware](https://expressjs.com/en/guide/using-middleware.html#middleware.router)**:Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router(). Load router-level middleware by using the router.use() and router.METHOD() functions.


2. **[Dynamic module MDN ](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#dynamic_module_loading)**: This allows you to dynamically load modules only when they are needed, rather than having to load everything up front. 



3. [Singleton Pattern](##What-does-Singleton-mean?)

4. **[CRUD -> REST Method Matches](https://medium.com/@ritika.atal.work/crud-mapping-to-http-verbs-354a3c0009f5)**: One can think of REST as the “CRUD for HTTP resources & more”- as long as one understands the difference between http resources and db records. REST is an API architecture which interacts with complex system whereas CRUD is a set of primitive operations which mostly manipulates data.



5. [**Mock Testing**](https://devopedia.org/mock-testing#:~:text=Mock%20testing%20is%20an%20approach,behaviour%20of%20the%20real%20ones.): is an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules. In mock testing, the dependencies are replaced with objects that simulate the behaviour of the real ones. The purpose of mocking is to isolate and focus on the code being tested and not on the behaviour or state of external dependencies.


________________________________________

## Securing Passwords

![password](https://thehackernews.com/images/-MtlGvP8uwLA/U0a9r7DfC7I/AAAAAAAAbIM/3ZH7rgjNuCM/s728/Cryptographic-hash-algorithms.jpg)

+ Passwords are the first line of defense against cyber criminals
+ It is the most vital secret of every activity we do over the internet and also a final check to get into any of your user account.
+ We all know storing passwords in clear text in your database is ridiculous.**that has to be stored using a hashing algorithm.**
+ Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3
+ The benefit of hashing is that if someone steals the database with hashed passwords, they only make off with the hashes and not the actual plaintext passwords.
+ weaknesses in cryptographic hash algorithm:
    - Brute Force attack.
    - Hash Collision attack.

+ This method of hashing passwords is solid enough for most web applications that stores users' passwords and other sensitive data.


_______________________________________

## Basic access authentication

* HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.

* The BA mechanism does not provide confidentiality protection for the transmitted credentials. They are merely encoded with Base64 in transit and not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.

## Authentication Cheat Sheet

* **Authentication** is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know

* Password managers are programs, browser plugins or web services that automate management of large number of different credentials. Most password managers have functionality to allow users to easily use them on websites, either by pasting the passwords into the login form, or by simulating the user typing them in.

* Web applications should at least not make password managers job more difficult than necessary by observing the following recommendations:
    - Use standard HTML forms for username and password input with appropriate type attributes.
    - void plugin-based login pages (such as Flash or Silverlight).
    - Implement a reasonable maximum password length, such as 64 characters.
    - Allow any printable characters to be used in passwords.
    - Allow users to paste into the username and password fields.
    - Allow users to navigate between the username and password field with a single press of the Tab key.

_________________________________________

## node.bcrypt.js

![node](https://i.morioh.com/200804/0adc4c0a.webp)

**A library to help you hash passwords.**

1. Verify that the node version you are using is a stable version
2. Security Issues And Concerns: As should be the case with any security tool, this library should be scrutinized by anyone using it. If you find or suspect an issue with the code, please bring it to my attention and I'll spend some time trying to make sure that this tool is as secure as possible.
3. Compatibility Note:This library supports $2a$ and $2b$ prefix bcrypt hashes. $2x$ and $2y$ hashes are specific to bcrypt implementation developed for John the Ripper. In theory, they should be compatible with $2b$ prefix.
