# Reading Notes

## API, Dynamo and Lambda

### What’s the difference between a FIFO and a standard queue?
FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.
______________________________

### What classic design pattern is best represented by event driven programming?
**Event Sourcing**:
* This pattern uses both triggering and data function of events to invoke a chain of application state changes and supply those changes with complete set of required data that are represented by events to all the components in the system.
* This feature is powerful for debugging and anomaly detection by allowing developers to investigate bad events and monitor unusual behaviors more precisely.

![img](https://miro.medium.com/max/1250/1*f08DUU7-TGcBgIGpBQtnwg.jpeg)

* the pattern solves some of the classic data consistency issues between inter-dependent distributed systems like data divergence and duplicates by deriving a system state view directly from the stream of events in the Event Store — a concept known as Materializing Views.

________________________________________

### How can the server be assured a message was properly received?

by **message authentication code (MAC)**, sometimes known as a tag, is a short piece of information used to authenticate a message—in other words, to confirm that the message came from the stated sender (its authenticity) and has not been changed. The MAC value protects a message's data integrity, as well as its authenticity, by allowing verifiers (who also possess the secret key) to detect any changes to the message content.
__________________________________

### How do you test an event driven system?

1. Unit tests are the most basic tests you will write. 
![](https://miro.medium.com/max/875/1*NdiTTk_s6-ignfVB0fBKLw.jpeg)

2. Service tests, as the name suggests, treat the entire service as the SUT, and increasingly, in microservice architectures this is where the bulk of automated testing occurs.

![](https://miro.medium.com/max/875/1*cF7xwAC1pIlpLly8FMXflg.jpeg)

3. End-to-end Tests:This is the ultimate ‘it works’ validation, that ensures that the contracts covered in the service tests ‘meet’.

![](https://miro.medium.com/max/875/1*wQCWYjKoLkn8SekOEStHmQ.jpeg)
______________________________________
## terms:

*  **Content Delivery Network (CDN)** is a geographically distributed group of servers that work together to provide fast delivery of Internet content.

* **Serverless functions** is the name given to a model of cloud computing where the developers have almost no overhead of managing infrastructure.

* **Cloud storage** is a model of computer data storage in which the digital data is stored in logical pools, said to be on "the cloud". The physical storage spans multiple servers (sometimes in multiple locations), and the physical environment is typically owned and managed by a hosting company.
_____________________________________________

## What is Amazon API Gateway?
![](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)


* is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. 

* API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. 

* API Gateway is the piece that ties together Serverless functions and API definitions. 

* Many AWS services support integration with Amazon API Gateway, including:

    * AWS Lambda: run Lambda functions to generate HTTP API responses.
    * AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.
    * Amazon Cognito: provide authentication and authorization for your HTTP APIs.

_________________________

![](https://d1.awsstatic.com/Test%20Images/MasonTests/Lambda_WebApplications.2139ddbc8a84f5564ee5846995f28c88e9db5c2d.png)

* **Dynamoose** is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

## Key Features
* Type safety
* High level API
*Easy to use syntax
* Ability to transform data before saving or retrieving documents
* Strict data modeling (validation, required attributes, and more)
* Support for DynamoDB Transactions
* Powerful Conditional/Filtering Support
* Callback & Promise support
