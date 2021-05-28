# Event Driven Applications

Event driven programming as a programing approach allows high control and scaleability on our applications. We usualy use event-driven programming without realizing that.

When we interact with a web page, we are causing events to be emitted and listened to. So, if we click on a button, this action emits a button-click event, and the browser will react to this event with whatever function and operations are passed to the event handler. Also, when we hover over some elements on the document interface or selecting a text we also cause events to be emitted and a respond to these events are run.

There are two main parts for event-driven programming make use of:

1. The main event-loop
2. The event handlers that respond to events

## Event Emitter with Node.js

Node is quite a decint tool that allows us to play aroud with events and include event-drived concept into our applications.
Node provides us with a native package called `events` Which we can use to emit events when they are come to happen.

```javascript

const EventEmitter = require('events').EventEmitter;
const events = new EventEmitter;

```

It is very useful to note that it is so much better to declare event-handling functions with valid names so we can reference them when we want to remove event listeners. This step is very important when we no longer need the event-handler and the event will not occure anymore.

## Why is access control important?

When we are building a website, different kinds of users have different accessibility to the website's content. The level of authorization will vary depending on the type of user. Therefore, access control is massively important to let our application decide and define each user and the content they are authorized to display and interact with.

## Describe an application that would need access control

Applications like accounting software need access control because many types of users are dealing with the application. Normal users would only be allowed to modify their personal information and read receipts or have a copy of them. Employees would have access to modify users' sensitive information and produce receipts, add new users to the system. Admin will have access to employees' data, change any kind of information they need, delete users, add new shops, etc.

## What is a role used for?

A role is a keyword that determines the level of accessibility of each user. So, some users are just normal users, and others are admins or employees. So, each one of the users should have in their information this keyword which is the role.

## Why is role-based access control more scalable than discretionary or mandatory access control?

Role-Based Access Control takes more of a real-world approach to structuring access control. Access under RBAC is based on a user's job function within the organization to which the computer system belongs.

Essentially, RBAC assigns permissions to particular roles in an organization. Users are then assigned to that particular role. For example, an accountant in a company will be assigned to the Accountant role, gaining access to all the resources permitted for all accountants on the system. Similarly, a software engineer might be assigned to the developer role.

Roles differ from groups in that while users may belong to multiple groups, a user under RBAC may only be assigned a single role in an organization. Additionally, there is no way to provide individual users additional permissions over and above those available for their role. The accountant described above gets the same permissions as all other accountants, nothing more and nothing less.

## Term

1. Authorization: Authorization is a security mechanism to determine access levels or user/client privileges related to system resources, including files, services, computer programs, data, and application features.
2. Role-Based Access Control: Role-Based Access Control (RBAC) is a security paradigm whereby users are granted access to resources based on their role in the company. RBAC, if implemented correctly, can be an effective way of enforcing the principle of least privilege.
3. Capabilities: it is a function that determines each role and its privileges according to the role keyword provided to the user object in software.
