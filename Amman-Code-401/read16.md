# AWS: Cloud Servers

## What a virtual machine is?

Computers are machines that perform high-level computing operations. Computers contain components called hardware, which are complicated to deal with. However, there is another component called the software that makes dealing with hardware easy and intuitive. There is a special kind of software called the operating system. This software is the interface to the hardware and deals directly with the components. Usually, computers need only one of these operating systems, and it is all set. On the other hand, sometimes we need to set up more than one operating system for special purposes.

A virtual machine is a process of having more than one operating system and making them working inside each other as if each was an individual machine on its own.

### Benefits of using multiple operating systems

1. Testing other applications
2. Trying new operating systems
3. Running old software that needs older operating system versions

### How to install Virtual Machines on the system

There are specialized pieces of software that allow us to do so. They are called hypervisors. We can put several VM's on one computer.

### Features

1. Fewer physical machines
2. Lower cost
3. Centralized management
4. Lower operating power

## What is Cloud Computing?

When we need more virtual machines than our computer can handle, we rent other computers that allow us to use their computing power and VM's hypervisors to complement our computer. It is like having your computer but far away from you to perform your computing tasks.

## Amazon EC2

Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure and resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides complete control of your computing resources and lets you run on Amazon’s proven computing environment.

## Review, Research, and Discussion

### Describe the Web-Request-Response-Cycle

The request/response cycle traces how a user’s request flows through the app. These are the steps of WRRC:

1. A user opens his browser, types in a URL, and presses Enter.
2. When a user presses Enter, the browser makes a request for that URL.
3. The request hits the router. The router maps the URL to the correct controller and action to handle the request.
4. The action receives the request and passes it on to the view.
5. The view renders the page as HTML.
6. The controller sends the HTML back to the browser. The page loads, and the user sees it.

### Explain what a “server” is as it relates to the WRRC?

It is the computer that HTTP requests are sent and from where the response is received.


### What does it mean to “deploy” an application?

When we deploy the application, we make it available online to go to its specific URL and benefit from the services it provides. Deploying involves storage and processing power to allow the application to run as it is running on one's personal machine.