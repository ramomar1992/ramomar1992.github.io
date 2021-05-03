# Express

## What’s the difference between PUT and PATCH?

PUT and PATCH are HTTP request methods that follow the RESTful design. Both methods perform modifications on the data we already have on the server, but there is one big difference. Put changes the whole record and delete the previous data completely. The patch is a little bit more flexible. It allows modifying part of the record without deleting the whole data set. So if there is relational data in a table and we want to modify a whole row in a table, we use PUT. If we only want to modify a special column of data in the row, we use PATCH.

## Provide links to 3 services or tools that allow you to “mock” an API for development like JSON-server

1. POSTMAN
2. INSOMNIA
3. MOCKOON
4. SuperTest
5. Mocha

## Compare and contrast SOAP and ReST

**REST**: refer to Representational State Transfer, it’s an architectural style that defines a set of recommendations for designing loosely coupled applications that use the HTTP protocol for data transmission.
It is an architectural style with loose guidelines and recommendations. It is data-driven (data available as resources, e.g., “user”), stateless (no server-side sessions). It allows API caching. Supports HTTPS and SSL. Requires fewer resources. Accepts plain text, HTML, XML, JSON, YAML, and others. Recommended for HTTP Public APIs for web services, mobile services, social networks. Has better scalability, better performance, browser-friendliness, flexibility. Scalability, better performance, Less security, not suitable for distributed environments.

**SOAP**: refer to Simple Object Access Protocol, it’s a standardized protocol that sends messages using other protocols such as HTTP. It returns data to the receiver in XML format. It is a standardized protocol with pre-defined rules to follow. It is function-driven (data available as services, e.g., “getUser”), stateless by default, but it’s possible to make a SOAP API stateful. API calls cannot be cached with it. It has WS-Security with SSL support, built-in ACID compliance. However, it requires more bandwidth and computing power, and it only accepts  XML. Suitable for enterprise apps, high-security apps, distributed environment, financial services, payment gateways, telecommunication services. Featured with high security, standardized, extensibility, but poorer performance, more complexity, less flexibility.

## Document the following Vocabulary Terms

* Web Server: a computer that is continuously running and connecting to the Internet. It serves clients and users with data and websites. It can contain a storage unit to act as a database for users' data.
* Express: it is an unopinionated, minimalist, and lightweight Node framework. It allows us to write server scripts on top of Node and use the HTTP request REST method to perform requests and respond to and from the server.
* Routing: it is the process of selecting a path for traffic in a network or between or across multiple networks. Broadly, routing is performed in many types of networks, including circuit-switched networks, such as the public switched telephone network (PSTN), and computer networks, such as the Internet.
* WRRC: web request-response cycle is a cycle that describes the flow of data between the client and the server or between the server and other servers. It starts with the user request from the front-end. The request is then transmitted to a DNS that provides a special IP address to the client. The client can then send the request to the IP address, a web server in this case. The web server does some processing for the test, and it can call other external APIs or get data from a database. After processing the data, the server response back to the client with a proper response in the form of files that build a web page or data to process or anything else.

## Q&A

1. Which three things had you heard about previously and now have better clarity on? 1. HTTP requests and responses. 2. Express implementations. 3. Agile and CI/CD.
2. Which three things are you hoping to learn more about in the upcoming lecture/demo? 1. Testing. 2. Data structure and Algorithms. 3. Coding interviews.
3. What are you most excited about trying to implement or see how it works? I want to build a full website with full implementation, including testing, and to be built in a perfect workflow.
