# Bearer Authorization

## Write the following steps in the correct order

1. Ask the client if they want to sign in via a third party
2. Make a request to a third-party API endpoint
3. Redirect to a third party authentication endpoint
4. Register your application to get a client_id and client_secret
5. Receive authorization code
6. Receive access token
7. Make a request to the access token endpoint

## What can you do with an authorization code?

* Send information securely
* Athorization

## What can you do with an access token?

Access tokens are used in token-based authentication to allow an application to access an API. The application receives an access token after a user successfully authenticates and authorizes access, then passes the access token as a credential when it calls the target API. The passed token informs the API that the bearer of the token has been authorized to access the API and perform specific actions specified by the scope that was granted during authorization.

## What’s a benefit of using OAuth instead of your own basic authentication?

Http Basic : This is for authentication and user credentials are encoded then passed in HTTP header to the client server. Basic example for HTTP Basic : Just like traditional web application which asked user to provide credentials and these credentials sent to server in HTTP header. Later server utilize those credentials to authenticate the user.

OAuth 2 : This is for authorization, here the client server required authorization of user data(resource owner) from authorization server. Basic example for OAuth 2 : Let say there is a online game application running on a server, the user accessed the application which starts loading into user's browser. Now that application asking grants from user to post data about games on his Facebook account. Here user authorize his that application to access his Facebook posts through OAuth Standard. Refer the internal mechanism

## Terms

1. Client ID: The client_id is a public identifier for apps. Even though it’s public, it’s best that it isn’t guessable by third parties, so many implementations use something like a 32-character hex string. It must also be unique across all clients that the authorization server handles. If the client ID is guessable, it makes it slightly easier to craft phishing attacks against arbitrary applications.
2. Client Secret: is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors. Protect your client secrets and never include them in mobile or browser-based apps.
3. Authentication Endpoint: Endpoint authentication is an authentication mechanism used to verify the identity of a network's external or remote connecting device. These endpoint devices include laptops, smartphones, tablets, and servers. This method ensures that only valid or authorized endpoint devices are connected to a network. These endpoint devices include laptops, smartphones, tablets and servers.
4. Access Token Endpoint: is where apps make a request to get an access token for a user.
5. API Endpoint: is a point at which an application program interface (API) -- the code that allows two software programs to communicate with each other -- connects with the software program. APIs work by sending requests for information from a web application or web server and receiving a response.
6. Authorization Code:  is a temporary code that the client will exchange for an access token. The code itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.
7. Access Token: is an object encapsulating the security identity of a process or thread. A token is used to make security decisions and to store tamper-proof information about some system entity.

## JWT (JSON Web Token)

* JSON Web Token (JWT) is an open standard (RFC 7519)
* compact and self-contained way for securely transmitting information between parties as a JSON object.
* digitally signed.
* sent through URL, POST request, HTTP Header
* can be encrypted to also provide secrecy between parties

## For what should you use JSON Web Tokens?

* Authorization: allowing the user to access routes, services, and resources that are permitted with that token.
* Information Exchange : JSON Web Tokens are a good way of securely transmitting information between parties.you can be sure the senders are who they say they are
