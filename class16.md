# Reading Notes 
## cloud server 

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

____________________________________

## Terms 

* **server** is a computer that provides data to other computers. It may serve data to systems on a local area network (LAN) or a wide area network (WAN) over the Internet. Many types of servers exist, including web servers, mail servers, and file servers. Each type runs software specific to the purpose of the server.

*  **publish–subscribe** is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. 

* **WRRC**:The web is a cycle of requests and responses that flow between clients and servers.

_______________________________________

## Cloud computing :

* Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment.

* Amazon EC2 Spot can reduce costs up to 90% or accelerate performance for fault-tolerant workloads such as big data, containers, web services, and CI/CD.
* AWS Savings Plans offers savings of up to 72% on Amazon EC2 instances usage, regardless of instance family, size, OS, tenancy or AWS Region.

* The AWS Region/AZ model has been recognized by Gartner as the recommended approach for running enterprise applications that require high availability. 

* Amazon EC2 offers the broadest and deepest compute platform with choice of processor, storage, networking, operating system, and purchase model.