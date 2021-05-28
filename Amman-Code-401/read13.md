# Message Queues

A message queue is a queue of messages sent between applications. It includes a sequence of work objects that are waiting to be processed. A message is the data transported between the sender and the receiver application; it's essentially a byte array with some headers at the top. It is a form of asynchronous service-to-service communication used in serverless and microservices architectures. Messages are stored on the queue until they are processed and deleted. Each message is processed only once, by a single consumer. Message queues can be used to decouple heavyweight processing, to buffer or batch work, and to smooth spiky workloads.

## Benifits of Message Queues

A message queue provides a lightweight buffer which temporarily stores messages, and endpoints that allow software components to connect to the queue in order to send and receive messages. The messages are usually small, and can be things like requests, replies, error messages, or just plain information.

Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

To send a message, a component called a producer adds a message to the queue. The message is stored on the queue until another component called a consumer retrieves the message and does something with it.

Many producers and consumers can use the queue, but each message is processed only once, by a single consumer. For this reason, this messaging pattern is often called one-to-one, or point-to-point, communications. When a message needs to be processed by more than one consumer, message queues can be combined with Pub/Sub messaging in a fanout design pattern.

## Features of Message Queue services

1. Asynchronous Messaging. Asynchronous messaging is a foundational concept for message queueing.
2. Unlimited Queues.
3. Real-Time Message Processing.
4. Push and Pull Queues.
5. First in, First out (FIFO).
6. One-Time Delivery.
7. Automatic Failover.
8. MQ as a Service.

## What does it mean that web sockets are bidirectional? Why is this useful?

It means that it allows the data to flow in both directions from the client to the server and from the server to the client simultaneously with reliability and consistency. It is useful because it allows us to form an open connection between two computers connected to the network and allows for real-time applications like chat apps and video call apps.

## Does socket.io use HTTP? Why?

Yes, it needs an HTTP connection to allows the first handshake in the open-system connection. It requires an HTTP server for the initial upgrade handshake. So even if you don't supply Socket.io with an HTTP server, it will create one for you.

## What happens when a client emits an event?

Some other event listeners will be listening to this event. If the event were emitted, it would trigger the event handler, doing some stuff and responding to the event.

## What happens when a server emits an event?

Some other event listeners will be listening to this event. If the event were emitted, it would trigger the event handler, doing some stuff and responding to the event.

## What happens if a client “misses” an event?

There will never be a response to this event, and the emitter will terminate without any significant changes in the application workflow.

## Terms

* Socket: it is a general term that refers to a data or power port that allows other data tracks to reach for and cause changes. In the web world, the socket is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to.
* Web Socket: is a computer communications protocol providing full-duplex communication channels over a single TCP connection.
* Socket.io: it is a package that allows us to use Websockets and other features when we build web applications. It enables real-time, bidirectional, and event-based communication.
* Client: it could be a browser (front-end) or a server with an open socket to the original server.
* Server: The computer contains the software that opens the serving socket to the client.
* OSI Model: stands for Open-System Integration model, is a model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.
* TCP Model: Transmission Control Protocol is the conceptual model and communications protocols used in the Internet and similar computer networks.
* TCP is a standard that defines establishing and maintaining a network conversation through which application programs can exchange data.
* UDP: User Datagram Protocol is a communications protocol primarily used to establish low-latency and loss-tolerating connections between applications on the internet. It is generally faster than TCP because it does not perform feedback checking on data received by the client.
* Packets: it is a form of data that consists of a small amount of information with a port number, IP addresses to the sender and the caller, and a tail part that contains some protocol information.
