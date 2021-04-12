# Reading Notes 

## Socket.io

![](https://socket.io/images/rooms.png)

### What is the benefit of transforming data into packets?

- More efficient in terms of bandwidth, since the concept of reserving circuit is not there.
- Minimal transmission latency.
- More reliable as destination can detect the missing packet.
- More fault tolerant because packets may follow different path in case any link is down, Unlike Circuit Switching.
- Cost effective and comparatively cheaper to implement.
_______________________________
### UDP is often refereed to as a connectionless protocol. Why is this?
UDP is a connectionless protocol. No connection needs to be established between the source and destination before you transmit data. UDP does not have a mechanism to make sure that the payload is not corrupted. As a result, the application must take care of data integrity all by itself.

___________________________________

### Can a socket server application have multiple socket connections?
A server socket listens on a single port and Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs, and the server would be able to handle as many clients as available system resources allow it to.

___________________________________

### Can a socket connection application be connected to multiple socket servers?
Yes but it need a separate connection factory for each server.

____________________
## Terms 

* Observer Pattern:is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

* **listener** is a procedure or function in a computer program that waits for an event to occur.

* **Event handlers** can be used to handle and verify user input, user actions, and browser actions: Things that should be done every time a page loads. Things that should be done when the page is closed. 

* **event-driven programming** is when a program is designed to respond to user engagement in various forms. 

* **Event Loop** has one simple job — to monitor the Call Stack and the Callback Queue. If the Call Stack is empty, the Event Loop will take the first event from the queue and will push it to the Call Stack, which effectively runs it.

* **event queue** is a repository where events from an application are held prior to being processed by a receiving program or system.

* **call stack** is a stack data structure that stores information about the active subroutines of a computer program.

* **Emit/Raise/Trigger** : in event-driven programming, emit sends a message to trigger a response and raise an event.

* **Subscribe** is a method that listens for a specific event that is raised by an event publisher.

* **A database** is a data structure that stores organized information. Most databases contain multiple tables, which may each include several different fields. 
 
________________________

#### Web Sockets

WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they are different, RFC 6455 states that WebSocket “is designed to work over HTTP ports 443 and 80 as well as to support HTTP proxies and intermediaries,” thus making it compatible with the HTTP protocol. To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header[1] to change from the HTTP protocol to the WebSocket protocol.

______________________

#### Socket.IO
Socket.IO enables real-time bidirectional event-based communication. It works on every platform, browser or device, focusing equally on reliability and speed. Socket.IO is built on top of the WebSockets API (Client side) and Node.js. It is one of the most depended upon library on npm (Node Package Manager).

____________________________

#### WebSocket vs Socket.io

* **Socket.IO** is a library which enables real-time and full duplex communication between the Client and the Web servers. It uses the WebSocket protocol to provide the interface. Generally, it is divided into two parts, both WebSocket vs Socket.io are event-driven libraries

* **WebSocket** is the communication Protocol which provides bidirectional communication between the Client and the Server over a TCP connection, WebSocket remains open all the time so they allow the real-time data transfer. When clients trigger the request to the Server it does not close the connection on receiving the response, it rather persists and waits for Client or server to terminate the request.