# The History of Web Storage and HTML5 Storage(DOM Storage)

Local storage has been one of the biggest concerns of web browser developers. Without the mechanism that allows browsers to store data locally on the client-side, the web application will have a shortage in speed and security. Unlike client native applications that can ultimately use local storage, web applications in the past were very limited to utilizing few kilobytes or megabytes. However, later versions of web browsers have wider capabilities and support for large amounts of space in the client machine.

## The history of local web storage methods

1. At the beginning of the widespread web, cookies were massively used among almost all web browsers out there. It was limited to 4kb, so it creates many major concerns about security and data transfer speed between client and server.
2. By the end of the 90s, Microsoft invented the concept of userData, which used a file format called the DHTML. It allowed storage up to 64kb, and in some trusted web applications, it was allowed to store 100kb.
3. In 2002, adobe introduced Flash 6, with the ability to store 100kb per domain, then in 2006, they re-wrote the library, and this allowed the usage of more than 100kb by prompting the user for each space magnitude needed, that can use up to 10 MB and 100 MB and so on.
4. Google launched Gears. It creates a SQL database locally on the client machine and allowed unlimited storage of data.

Every one of these methods has their limitation, and in the end, each one of them is presented on one browser with different API which in turn lead to different user experience. Here where HTML5 came in handy and solved all problems related to local storage and the ability to integrate its specifications in all browsers.

## HTML5 Web Storage (DOM Storage)

It is a way to store data in key/value pairs, and it stays stored even when the browser tab is closed, navigated away from the website, or even close the whole browser window. Unlike cookies, however, it is not transmitted to the server. It also works even when the browser does not support third-party plugins because it is implemented natively in the web browser. All major browsers also support it.

- To access the local storage using javascript, you should use the localStorage element on the window object.

- When you want to retrieve data from the local storage, you need to use the key name stored in a string. All data are retrieved in string format even if it was numbered or boolean values; therefore, you need to cast it into data type conversions like parseInt or parseFloat.

- Use getItem method or square brackets to get values for the key you specify in the brackets. Use setItem or the square brackets with assignment operator to overwrite or create new data pair.

- Use the clear method to erase all the values presented in the storage, or removeItem with its key to remove specified data pair.