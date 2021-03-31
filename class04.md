# Reading-Notes 

## Data Modeling

![datamodeling](https://dataedo.com/asset/img/banners/blog/modeling_techniques.png)

_________________________________

### 3 advantages to Test Driven Development
![TDD](https://codica-images-staging.s3.eu-central-1.amazonaws.com/c3cb64e3ac2d4eae89002e0ccc5789dd.png)

1. Better program design and higher code quality.
2. TDD reduces the time required for project development
3. Code flexibility and easier maintenance


[for more information](https://www.codica.com/blog/test-driven-development-benefits/)

___________________________________

### what case would you need to use beforeEach() or afterEach() in a test suite?

when writing the test you need to check the for the setup before and after the test  
The difference is beforeEach()/afterEach() automatically run before and after each tests, which 
1. removes the explicit calls from the tests themselves
2. invites inexperienced users to share state between tests.
_______________________________

###  one downside of Test Driven Development:
* No silver bullet –Tests help to seek out bugs, but they can not find bugs that you simply introduce within the test code and in implementation code. If you haven’t understood the matter you would like to unravel, writing tests most likely doesn’t help.

__________________________________

### primary difference between ES6 Classes and Constructor/Prototype Classes

* Classes can’t be called without new, but functions intended as constructors can (and their this will be wrong)

* Classes can extend more types than constructors can (like functions and arrays)

* Classes’ prototypes are their parents (they inherit static properties); writers of constructor functions usually don’t bother with this

* Non-classes can’t extend classes (because they can’t call the parent constructor – see the first point)

_________________________________

### Why REST? 

![REST](https://lh3.googleusercontent.com/A2bb3UwAu4u9UU1q9FdUgZ9MAfnain306RndVW7sRXWumQ0FVVM4XhGDRTtr0YYDSBULrewxtAqKdmZUPFUKXF2g6NY3fCg2vLGyLZxaFIpOJ5Oi8MzLgiNyJIJwsIyq2RRCabkp)

The advantages of REST for development:

1. Separation between the client and the server: the REST protocol totally separates the user interface from the server and the data storage. This has some advantages when making developments. For example, it improves the portability of the interface to other types of platforms, it increases the scalability of the projects, and allows the different components of the developments to be evolved independently.

2. Visibility, reliability and scalability. The separation between client and server has one evident advantage, and that is that each development team can scale the product without too much problem. They can migrate to other servers or make all kinds of changes in the database, provided the data from each request is sent correctly. The separation makes it easier to have the front and the back on different servers, and this makes the apps more flexible to work with.

3. The REST API is always independent of the type of platform or languages: the REST API always adapts to the type of syntax or platforms being used, which gives considerable freedom when changing or testing new environments within the development. With a REST API you can have PHP, Java, Python or Node.js servers. The only thing is that it is indispensable that the responses to the requests should always take place in the language used for the information exchange, normally XML or JSON. 

________________________

![JS](https://hackernoon.com/hn-images/1*bxEkHw1xewxOFjmGunb-Cw.png)

## What is?

* **functional programming:**is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects.And is declarative rather than imperative, and application state flows through pure functions.

* **object-oriented programming (OOP):** Object-oriented programming (OOP) is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior.

*  **A class** is written by a programmer in a defined structure to create an object (computer science) in an object oriented programming language. It defines a set of properties and methods that are common to all objects of one type.

* **The super** keyword is used to access and call functions on an object's parent.


_____________________________

* Data Model is an abstract model that organizes elements of data and standardizes how they relate to one another and to the properties of real-world entities.


___________________________

## SQL vs NoSQL:

|  SQL     |  NoSQL: |
| ----------- | ----------- |
| relational      | non-relational      |
| predefined schema | dynamic schemas      |
| vertically scalable   | horizontally scalable      |
| table based   | document, key-value, graph or wide-column stores.        |
| better for multi-row transactions   | better for unstructured data like documents or JSON.        |


______________________________________


## NOSQL DATA MODELING TECHNIQUES:

1. Denormalization: Denormalization can be defined as the copying of the same data into multiple documents or tables in order to simplify/optimize query processing or to fit the user’s data into a particular data model.

2. Application Side Joins: Joins are rarely supported in NoSQL solutions. As a consequence of the “question-oriented” NoSQL nature, joins are often handled at design time as opposed to relational models where joins are handled at query execution time.

