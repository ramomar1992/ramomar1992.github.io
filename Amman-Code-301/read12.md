# EJS Partials

Partials are essential parts of EJS. They allow us to write chunks of code once and use them on multiple pages.

We write the reusable code in a separate file, and then we include it inside another one. Then, when we run it, the code will work as if it was initially there.

There is a special EJS delimiter to use when including the partials in other files, which is `<%- include(file-path) %>`.

We usually use partials for HTML elements in all website pages like headers, footers, and sides. Partials are incredibly useful. They benefit us in:

* Code reusability
* Modularity
* Consistency
* Code faster
