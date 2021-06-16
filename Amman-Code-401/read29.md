# React Routing

* React Router has been broken into three packages: react-router, react-router-dom, and react-router-native.
* If we are building a website (something that will be run in browsers), so we will install react-router-dom.
* The \<BrowserRouter> should be used when you have a server that will handle dynamic requests (knows how to respond to any possible URI), while the \<HashRouter> should be used for static websites (where the server can only respond to requests for files that it knows about).
* A React Router component that does not have a router as one of its ancestors will fail to work.
* Router components only expect to receive a single child element. To work within this limitation, it is useful to create an \<App> component that renders the rest of your application.
* The \<Route> component is the main building block of React Router. Anywhere that you want to only render content based on the location’s pathname, you should use a \<Route> element.

## Path names

A \<Route> expects a path prop, which is a string that describes the pathname that the route matches — for example, \<Route path='/roster'/> should match a pathname that begins with /roster. When the current location’s pathname is matched by the path, the route will render a React element. When the path does not match, the route will not render anything.

When it comes to matching routes, React Router only cares about the pathname of a locatio

## Routers Organiztion

\<Route>s can be created anywhere inside of the router, but often it makes sense to render them in the same place. You can use the \<Switch> component to group \<Route>s. The \<Switch> will iterate over its children elements (the routes) and only render the first one that matches the current pathname.

In order to match a path in our application, all that we have to do is create a \<Route> element with the path prop we want to match.

## What does the \<Route> render?

Routes have three props that can be used to define what should be rendered when the route’s path matches. Only one should be provided to a \<Route> element.

1. component — A React component. When a route with a component prop matches, the route will return a new element whose type is the provided React component (created using React.createElement).
2. render — A function that returns a React element. It will be called when the path matches. This is similar to component, but is useful for inline rendering and passing extra props to the element.
3. children — A function that returns a React element. Unlike the prior two props, this will always be rendered, regardless of whether the route’s path matches the current location.

The element rendered by the \<Route> will be passed a number of props. These will be the match object, the current location object 6, and the history object (the one created by our router).

It can be useful to group routes that share a common prefix in the same component. This allows for simpler parent routes and gives us a place to render content that is common across all routes with the same prefix.

## Path params

Sometimes there are variables within a pathname that we want to capture. For example, with our player profile route, we want to capture the player’s number. We can do this by adding path params to our route’s path string.

## Links

To navigate between pages, if we were to create links using anchor elements, clicking on them would cause the whole page to reload. React Router provides a \<Link> component to prevent that from happening. When clicking a \<Link>, the URL will be updated and the rendered content will change without reloading the page.

\<Link>s use the to prop to describe the location that they should navigate to. This can either be a string or a location object (containing a combination of pathname, search, hash, and state properties). When it is a string, it will be converted to a location object.
