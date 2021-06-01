# API, Dynamo and Lambda

## Amazon API Gateway

Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, CORS support, authorization and access control, throttling, monitoring, and API version management. API Gateway has no minimum fees or startup costs. You pay for the API calls you receive and the amount of data transferred out and, with the API Gateway tiered pricing model, you can reduce your cost as your API usage scales.

### How it work

API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends.

It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services.

It can also generate API references from your definitions and make them available to your users as API documentation.

These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.

### The benefits of API Gateway

1. It integrates with other serverless services which allows to build a full web application
2. It allows execution of a serverless function in response to HTTP requests
3. Highly scaleable
4. Low maintainance
5. Less over head and cost
6. Map HTTP requests to specific functions in a Serverless application viaanAPI Gateway event.
7. Map WebSocket events to Serverless functions
8. Use multiple microservices to serve the same top-level API

## DynamoDB

### What is DynamoDB

DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS).

DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.

DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.

### Features of DynamoDB

1. Reliable performance
2. Managed experience
3. Small, simple API allowing for simple key-value access as well as more advanced query patterns.
4. No servers to manage

### What is it used for?

1. Applications with large amounts of data and strict latency requirements
2. Serverless applications using AWS Lambda
3. Data sets with simple, known access patterns
