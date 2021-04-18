# Reading Notes

## AWS: S3 and Lambda

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

* **server instance** is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based.

* **container** is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. ... Available for both Linux and Windows-based applications, containerized software will always run the same, regardless of the infrastructure.

* **Cloud services** are services available via a remote cloud computing server rather than an on-site server. These scalable solutions are managed by a third party and provide users with access to computing services such as analytics or networking via the internet.

* **Cloud Architecture** refers to the various components in terms of databases, software capabilities, applications, etc. engineered to leverage the power of cloud resources to solve business problems. 

* **Amazon Web Services** offers reliable, scalable, and inexpensive cloud computing services.

* **EC2/Beanstalk vs Heroku** One big difference is that Heroku’s pricing takes exponential price jumps as one adds common additional features, e.g., auto-scaling, where-as AWS pricing is fairly linear. On the other hand, Heroku is generally simpler to get up and running as AWS has a fairly steep initial learning curve.

______________________________________

## Amazon S3
* Amazon S3 is an object storage service that offers industry-leading scalability, data availability, security, and performance.

### Benefits
1. Industry-leading performance, scalability, availability, and durability
2. Wide range of cost-effective storage classes
3. Unmatched security, compliance, and audit capabilities
4. Easily manage data and access controls
5. Query-in-place and process on-request
6. Most supported cloud storage service


### Use cases:

1. Backup and restore
2. Disaster recovery (DR)
3. Archive
4. Data lakes and big data analytics
5. Hybrid cloud storage
6. Cloud-native applications
___________________________________

## AWS Lambda

* AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.

* building Serverless applications to complete a Serverless stack you’ll need:
    - a computing service;
    - a database service; and
    - an HTTP gateway service.

* Some of the most common use cases for AWS Lambda that fit these criteria are:
    - Scalable APIs.
    - Data processing. 
    - Task automation.
_______________________________________

## Content Delivery Network (CDN)

![](https://cyberhoot.com/wp-content/uploads/2020/03/What-is-Content-Delivery-Network-768x485.jpg)

*  **Content Delivery Network (CDN)** is a geographically distributed group of servers that work together to provide fast delivery of Internet content.

* What does this mean for an SMB?
CDNs are something that larger companies are more likely to implement. The main reasons why company want to use CDNs are to improve Internet website load speeds, content delivery speeds, and to reduce the likelihood of falling victim to and improve defenses against Distributed Denial of Service attacks (DDoS).

![](http://www.yuvacloud.com/wp-content/uploads/2019/03/cdn.jpg)



