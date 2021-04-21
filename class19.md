
# Reading Notes 

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

____________________________

* **Serverless API** is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers

* **Triggers**	is procedural code that is automatically executed in response to certain events on a particular table or view in a database.

* **Dynamo vs Mongo** is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas

* **Dynamoose vs Mongoose**	is a modeling tool for Amazon’s DynamoDB (inspired by Mongoose)

_____________________________

## AWS — Difference between SQS and SNS
1. SNS (Simple Notification Service)
![](https://miro.medium.com/max/625/1*mdUPKzrfJFuXa4d43KhKUQ.png)

* SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.


2. SQS ( Simple Queue Service)

![](https://miro.medium.com/max/625/1*7eL3udb6Cto4I9Ly1sN8oA.jpeg)

* SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages.


### Differences:

* Entity Type
SQS : Queue (Similar to JMS)
SNS : Topic (Pub/Sub system)

* Message consumption
SQS : Pull Mechanism — Consumers poll and pull messages from SQS
SNS : Push Mechanism — SNS Pushes messages to consumers

* Use Case
SQS : Decoupling two applications and allowing parallel asynchronous processing
SNS : Fanout — Meaning allowing same message to be processed in multiple ways

* Persistence
SQS : Messages are persisted for some (configurable) duration is no consumer available
SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.
In SQS the message delivery is guaranteed but in SNS it is not.

* Consumer Type
SQS : All the consumers are supposed to be identical and hence process the messages in exact same way
SNS : All the consumers are (supposed to be) processing the messages in different ways

* Sample applications
SQS : Jobs framework. Where the Jobs are submitted to SQS and the consumers at the other end can process the jobs asynchronously. And if the job frequency increases then the number of consumers can be increased for parallel processing
SNS : Image processing. If someone uploads an image to S3 then watermark that image, create a thumbnail and also send a ThankYou email. In that case S3 can send notification to SNS Topic and 3 consumers can be attached to SNS topic. 1st one watermarks the image, 2nd one creates a thumbnail and the 3rd one send a ThankYou email. All of them receiving the same message (image URL) and doing their corresponding processing in parallel.