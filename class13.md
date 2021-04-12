# Reading Notes
## Message Queues

![](https://secureservercdn.net/160.153.138.177/dxa.0a2.myftpupload.com/wp-content/uploads/2018/07/message-queue-small.png?time=1607877977)


### What does it mean that web sockets are bidirectional? Why is this useful?

- **BIDIRECTIONAL.** Whereas HTTP relies on a client request to receive a response from the server for every exchange,
WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates
asynchronously, without requiring the client to submit a request each time. In the context of networked AV and control
systems, this allows devices to send and receive continuous streams of data to and from any point on the network.

- The WebSocket protocol’s numerous advantages over HTTP make it effective in a variety of applications, including
networked AV and control systems. The protocol’s persistent connection and fully bidirectional nature enables a range of
web services, hardware devices and distributed systems to work together seamlessly.

[for more information](https://www.amx.com/en-US/site_elements/benefits-and-applications-of-websockets)

______________________

### Does socket.io use HTTP? Why?
 a socket.io server will attach to an HTTP server so it can serve its own client code through /socket.io/socket.io.js 
___________________________
 
### What happens when a client emits an event?
### What happens when a server emits an event?
The event gets passed to the server through websockets. Its a tcp connection from the browser to the server. **The connection is full duplex meaning the server can send real time data to the client and vise versa**.

- note the bold font is answering both questions
_________________________________

### What happens if a client “misses” an event?
Near Miss – An event that could have caused harm, loss and damage, but fortunately did not do so on this particular occasion.

________________________________

### [How can we mitigate this?](https://clutch.co/web-developers/resources/6-steps-mitigate-software-risks)

1. Track risks before they escalate, becoming issues that derail a development project
2. Address the riskiest parts of the development process first
3. Tackle risks immediately by using an Agile development approach
4. Create plans for potential risks at the beginning of the project, and share all risks with clients to be transparent
5. Track development and client team temperature metrics along with project timeline, budget, and scope
6. Encourage open communication and feedback throughout the development process to maintain team morale

________________________________

## Terms:
* **socket** is one endpoint of a two-way communication link between two programs running on the network.
* **WebSocket API** is an advanced technology that makes it possible to open a two-way interactive communication session between the user's browser and a server.
* **client** is a piece of computer hardware or software that accesses a service made available by a server as part of the client–server model of computer networks. The server is often on another computer system, in which case the client accesses the service by way of a network.

* **server** is a computer that provides data to other computers. It may serve data to systems on a local area network (LAN) or a wide area network (WAN) over the Internet.

* **OSI Model** (Open Systems Interconnection Model) is a conceptual framework used to describe the functions of a networking system. The OSI model characterizes computing functions into a universal set of rules and requirements in order to support interoperability between different products and software.

* **tcp model** It stands for Transmission Control Protocol/Internet Protocol. The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike seven layers in the OSI model. The layers are: Process/Application Layer.

* **TCP (Transmission Control Protocol)** is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other.

* **UDP (User Datagram Protocol)** is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.

* **packet** is a small amount of data sent over a network, such as a LAN or the Internet. Similar to a real-life package, each packet includes a source and destination as well as the content (or data) being transferred.

___________________________________

![](https://blog.crowdbotics.com/content/images/2020/04/nodesocketfeaturedimage.png)


### Rooms:
* A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients:

![](https://socket.io/images/rooms.png)


#### Please note that rooms are a server-only concept (i.e. the client does not have access to the list of rooms it has joined).

* Joining and leaving:
    - You can call join to subscribe the socket to a given channel
    - And then simply use to or in (they are the same) when broadcasting or emitting
    - In that case, a union is performed: every socket that is at least in one of the rooms will get the event once (even if the socket is in two or more rooms).
    - You can also broadcast to a room from a given socket
    - In that case, every socket in the room excluding the sender will get the event.
    - To leave a channel you call leave in the same fashion as join.


![](https://socket.io/images/rooms2.png)


* Room events
1. create-room (argument: room)
2. delete-room (argument: room)
3. join-room (argument: room, id)
4. leave-room (argument: room, id)

