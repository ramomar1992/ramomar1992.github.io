# Socket.IO

Socket.IO is a JavaScript library for real-time web applications. It enables real-time, bi-directional communication between web clients and servers. It has two parts: a client-side library that runs in the browser, and a server-side library for node.js. Both components have an identical API.

### Real-time applications
A real-time application (RTA) is an application that functions within a period that the user senses as immediate or current.

#### Some examples of real-time applications are −

* Instant messengers − Chat apps like Whatsapp, Facebook Messenger, etc. You need not refresh your app/website to receive new messages.

* Push Notifications − When someone tags you in a picture on Facebook, you receive a notification instantly.

* Collaboration Applications − Apps like google docs, which allow multiple people to update same documents simultaneously and apply changes to all people's instances.

* Online Gaming − Games like Counter Strike, Call of Duty, etc., are also some examples of real-time applications.

### Why Socket.IO?
Writing a real-time application with popular web applications stacks like LAMP (PHP) has traditionally been very hard. It involves polling the server for changes, keeping track of timestamps, and it is a lot slower than it should be.

Sockets have traditionally been the solution around which most real-time systems are architected, providing a bi-directional communication channel between a client and a server. This means that the server can push messages to clients. Whenever an event occurs, the idea is that the server will get it and push it to the concerned connected clients.

Socket.IO is quite popular, it is used by Microsoft Office, Yammer, Zendesk, Trello, and numerous other organizations to build robust real-time systems. It one of the most powerful JavaScript frameworks on GitHub, and most depended-upon NPM (Node Package Manager) module. Socket.IO also has a huge community, which means finding help is quite easy.

# WebSocket

WebSocket is a computer communications protocol, providing full-duplex communication channels over a single TCP connection.

WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they are different, RFC 6455 states that WebSocket "is designed to work over HTTP ports 443 and 80 as well as to support HTTP proxies and intermediaries," thus making it compatible with HTTP. To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header to change from the HTTP protocol to the WebSocket protocol.

The WebSocket protocol enables interaction between a web browser (or other client application) and a web server with lower overhead than half-duplex alternatives such as HTTP polling, facilitating real-time data transfer from and to the server. This is made possible by providing a standardized way for the server to send content to the client without being first requested by the client, and allowing messages to be passed back and forth while keeping the connection open. In this way, a two-way ongoing conversation can take place between the client and the server. The communications are usually done over TCP port number 443 (or 80 in the case of unsecured connections), which is beneficial for environments that block non-web Internet connections using a firewall. Similar two-way browser-server communications have been achieved in non-standardized ways using stopgap technologies such as Comet.

Most browsers support the protocol, including Google Chrome, Firefox, Microsoft Edge, Internet Explorer, Safari and Opera.

Unlike HTTP, WebSocket provides full-duplex communication Additionally, WebSocket enables streams of messages on top of TCP. TCP alone deals with streams of bytes with no inherent concept of a message. Before WebSocket, port 80 full-duplex communication was attainable using Comet channels; however, Comet implementation is nontrivial, and due to the TCP handshake and HTTP header overhead, it is inefficient for small messages. The WebSocket protocol aims to solve these problems without compromising the security assumptions of the web.

The WebSocket protocol specification defines ws (WebSocket) and wss (WebSocket Secure) as two new uniform resource identifier (URI) schemes that are used for unencrypted and encrypted connections, respectively. Apart from the scheme name and fragment (i.e. # is not supported), the rest of the URI components are defined to use URI generic syntax.

Using browser developer tools, developers can inspect the WebSocket handshake as well as the WebSocket frames.
