* How Rails knows which type of file you are expecting back when you make an HTTP request.

* What is the purpose of the `#respond_to` method?
  - to determine which file types the controller will respond to

* How do you return a User object but specify that you don’t want to include certain attributes (i.e. you can’t just return User.first)?
  1. change/override the `as_json` method with options
    `only: [:name, :email]`
  2. use inplace in the controller

* What are the two steps performed behind the scenes by the `#to_json` method?
  - `to_json` first invoke the `as_json` method to convert objects to hash of values

* How do you tell a controller action to render nothing but an error message?

* How do you build your own custom error messages?

* Why can’t you use session-based controller authentication methods if you want people to access your API programmatically?

* What is “Service Oriented Architecture?”
  > Your Application will likely have many defferent services within it, for instance payments processing, user registration, recommendation engine, etc.
  > Instead of building all of these under the same master application, you break them out into fully independent pieces and have them talk to each other using internally facing APIs.
  * Pros
    - Each piece works independently via ther APIs
    - Make changes to one service doesn't affect others
  * Cons