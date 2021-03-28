# Reading notes 401

## Express 

### PUT vs Patch :

* What is PUT? 
***PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PUT is similar to POST in that it can create resources, but it does so when there is a defined URI. PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn’t exist.For example, when you want to change the first name of a person in a database, you need to send the entire resource when making a PUT request.To make a PUT request, you need to send the two parameters; the first and the last name.***

* What is PATCH?
***PATCH applies a partial update to the resource.This means that you are only required to send the data that you want to update, and it won’t affect or change anything else. So if you want to update the first name on a database, you will only be required to send the first parameter; the first name.***

* Similarities between PUT and PATCH
The only similarity between the two is that they can both be used to update resources in a given location.

* Differences between PUT and PATCH
    1. The main difference between PUT and PATCH requests is witnessed in the way the server processes the enclosed entity to update the resource identified by the Request-URI. When making a PUT request, the enclosed entity is viewed as the modified version of the resource saved on the original server, and the client is requesting to replace it. However, with PATCH, the enclosed entity boasts a set of instructions that describe how a resource stored on the original server should be partially modified to create a new version.

    2. The second difference is when it comes to idempotency. HTTP PUT is said to be idempotent since it always yields the same results every after making several requests. On the other hand, HTTP PATCH is basically said to be non-idempotent. However, it can be made to be idempotent based on where it is implemented.


### 3 services or tools that allow you to “mock” an API for development:

1. [ Nock ](https://github.com/nock/nock)
2. [ Mock Server ](https://www.mock-server.com/)
3. [ Beeceptor ](https://beeceptor.com/)

### The main differences between SOAP and REST
SOAP and REST both allow you to create your own API. API stands for Application Programming Interface. It makes it possible to transfer data from an application to other applications. An API receives requests and sends back responses through internet protocols such as HTTP, SMTP, and others.

Many popular websites provide public APIs for their users, for example, Google Maps has a public REST API that lets you customize Google Maps with your own content. There are also many APIs that have been created by companies for internal use.

for more follow this link :
[ SOAP vs REST ](https://raygun.com/blog/soap-vs-rest-vs-json/#:~:text=As%20opposed%20to%20SOAP%2C%20REST,protocol%20but%20an%20architectural%20style.&text=It%20allows%20different%20messaging%20formats,services%20have%20a%20better%20performance.)


### API response :

![api](https://s3.us-west-1.wasabisys.com/idbwmedia.com/images/api/nonref_statuscodes.svg)


### SWAGGER response :
responses:
- '200': description: OK
- '400': description: Bad request. User ID must be an integer and larger than 0.
- '401': description: Authorization information is missing or invalid.
- '404': description: A user with the specified ID was not found.
- '5XX':description: Unexpected error.


## What is ?
* Web Server: A web server is server software, or a system of one or more computers dedicated to running this software, that can satisfy client HTTP requests on the public World Wide Web or also on private LANs and WANs.

* Express:Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.

* Routing: A Javascript router is a key component in most frontend frameworks. It is the piece of software in charge to organize the states of the application, switching between different views. For example, the router will render the login screen initially, and when the login is successfull it will perform the transition to the user’s welcome screen.






