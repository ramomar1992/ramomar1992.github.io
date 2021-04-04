# EJS

EJS or Embedded JavaScript is a templating technique that lets us create dynamic web pages with minimal code. It consists of some packages and modules that run for Node.js. To work with EJS, we have to install the package from NPM, and then we must include the package by setting the view engine header to EJS. We also set another header which is the views header, by passing the path to a folder where all .ejs files reside, and it should be name views. A best practice is to set the path to call a function imported from the path module installed as a dependency for express `path.join(__dirname,'views')`.

EJS is a template system. You define HTML pages in the EJS syntax, and you specify where various data will go on the page. Then, your app combines data with the template and "renders" a complete HTML page where EJS takes your data and inserts it into the web page according to how you've defined the template.

It is featured to be very easy and simple language besides the huge support to almost all browsers. It is fast to deploy and debug, as well as it is fast to be rendered on the web page—also, the use of plane JavaScript with it.

Some of the important features o EJS:

* Fast compilation and rendering
* Simple template tags: `<% %>`
* Custom delimiters like [? ?] instead of `<% %>`
* Sub-template includes
* Comes with CLI
* Both server JS and browser support
* Static caching of intermediate JavaScript
* Static caching of templates
* Complies with the Express view system
