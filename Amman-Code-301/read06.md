# NODE.JS

Node is a Javascript runtime that allows running applications written in javascript outside browsers using CHROME V8 Engine. It has so many features. It is asynchronous, non-blocking, and event-based.

To be able to run applications with Node, we have to install it on our machine. This is done in two ways. Either we install the latest version from the official website or install a version control, which contains more than one version, and it is helpful to run all kinds of applications.

We can now run any Javascript file directly in the terminal with the command ` Node <filename.js>`. This is easy. Node has excellent support to ES6, and we can write the most modern Javascript code, and it will run on Node without any problem. This means that we can use the arrow function, classes, template literals, object destructuring, filter and mapping, and more. 

When we install Node, it comes bundled with a package manager called NPM. Using this package manager, we can fetch and install over a million packages online. A package is a previously written JS code that people wrote and published online so that other developers can use it in their code. 

There is a file called `package.json` that should be included in our application where it has the names of the packages we want to use in our application, and when the NPM sees this file, it will fitch the section where the names of these packages are then it will download and install all of them one by one.
To have this file automatically created for us, we have to run the command `npm init`. It will then asks us some questions that we need to answer, or we can simply ignore them and type `npm init -y`. When we install any new package, the package's name and its version will be added automatically under dependences entry. 

We use Node to run applications on servers. Using Node is better than any other platform because it is asynchronous and event-based, which means it will not block the I/O operation to wait for other computing processes to finish first. Instead, it creates callbacks and queues them into a processing unit, and then when the call stack is empty, it will hand these callbacks over to the event loop to execute them in order. 

The best apps to built using Node are those that need real-time interaction, such as processing documents online while other people are watching. It has huge use in building APIs where we handle a lot of HTTP requests and I/O operations. Also, it is hugely helpful for applications that involve data streaming as it allows the processing of files while uploading.

Some libraries and frameworks simplify building applications using Node, and one of the most common ones is Express.js. Express alone is not enough to build extraordinary applications, so we need to get more useful modules from NPM and cooperate with Express and Node.

Other uses of Node: 

* Automating repetitive and error-prone tasks on pcs.
* Write our own command line code
* Creating cross-platform desktop apps.