# Access Control (ACL)

## When is Basic Authorization used vs. Bearer Authorization?

It is used when we want to add more layers of security to the tokens that come from the bearer security. Also, there is a big difference between the basic and the bearer auths. Basic auth is used when the user wants to sign in to the system, their information will be secured and encrypted, and we want to match their credentials with the information we already have in the database. On the other hand, Bearer auth is to keep the user signed across our website and not keep asking them to enter their credentials each time they want to reach for a route. Here web tokens will be saved in the cookies or fitched from the database to allow the user to navigate freely throughout the website when they are authenticated.

## What does the JSON Web Token package do?

It contains the functions and the objects needed to generate the web token from the user information and the secret code that the programmer has previously determined in the environment variables. The function is called `jwt.sign(info, secret)`. Another important function decodes the tokens to allow us to verify that the entered token matches one of the user tokens saved in the database. This method is `jwt.verify(token, secret)`. If the token is valid, the method will return an object that contains the username information and credentials. We then can search the database for a user name that matches the user name yield from the method. If there is one, we grant access to the user.

## What considerations should we make when creating and storing a SECRET?

* Use encryption to store secrets within .git repositories
* Use “Secrets as a service” solutions
* It should be stored securely
* It should be random, not guessable
* It should be a String

## TERMS

1. encryption: is the process of taking plain text, like a text message or email, and scrambling it into an unreadable format — called “ciphertext.” This helps protect the confidentiality of digital data either stored on computer systems or transmitted through a network like internet.
2. token: it’s a string used to authorize the user in the system
3. bearer: This is an HTTP authentication scheme created as part of OAuth 2.0 but is now used independently.
4. secret: a key added when generating the token as part of it to secure it more.
5. JSON Web Token:  is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.
