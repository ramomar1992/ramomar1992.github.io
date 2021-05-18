# Access Control (ACL)

## When is Basic Authorization used vs. Bearer Authorization?

It is used when we want to add more layers of security to the tokens that comes from the bearer security. Also there is a big difference between the basic and the bearer auths. Basic auth is used when the user wants to sign in to the system, their information is going to be secured and encrypted, and we want to match their cridenctials with the information we already have in the database. On the other hand, Bearer auth is to keep the user signed in across our website and not keep asking them to enter their cridentials each time they want to reach for a route. Here web tokens will be saved in the cookies or fitched from the database to allow the user to navigate freely throughout the website when they are authenticated.

## What does the JSON Web Token package do?

It contains the functions and the objects needed to generate the web token from the user information and the secret code that the programmer has previously determained in the environment variables. The function is called `jwt.sign(info, secret)`. There is also another important function that decode the tockens to allow us to verify that the entered token matches one of the user tokens saved in the database, this method is `jwt.verify(token, secret)`. If the token is valid the method will return an object that contains the username informaton and cridentials, we then can search the database for a user name that matches the user name yeld from the method and if there is one, we grant access to the user.

## What considerations should we make when creating and storing a SECRET?

* Use encryption to store secrets within .git repositories
* Use “Secrets as a service” solutions
* It should be stored securely
* It should be random, not guessable
* It should be a String

## TERMS

1. encryption: is the process of taking plain text, like a text message or email, and scrambling it into an unreadable format — called “cipher text.” This helps protect the confidentiality of digital data either stored on computer systems or transmitted through a network like the internet.
2. token: it’s a string used to authorize the user in the system
3. bearer: is an HTTP authentication scheme originally created as part of OAuth 2.0, but is now used on its own.
4. secret: a key that is added when generating the token as part of it to scure it more.
5. JSON Web Token:  is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
