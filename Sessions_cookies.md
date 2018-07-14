# Sessions, cookies, and authentication

`#rails` `#sessions` `#cookies` `#authentication`

* What is a session?
  > Session is a place to store data during one request that you can read during later requests 

* How is the session “hash” different from the cookies “hash”?

* What is the flash “hash” used for?
  > Flash is a hash (a method that acts like a hash) that persists only from one request to the next

* When would you need to use flash.now instead of flash?
  > adding values to flash make them available to the next request
  > adding values to flash.now make them available now in current request

* What are controller filters and why are they useful?
  > Filters are methods that are run `before`, `after` or `around` a controller action.
  > Filters are inherited, so if you set a filter in ApplicationController, it will be run on every controller in your appliaction.

* How do you run a controller filter for just a specific few actions?
  > use only: option

* What’s the difference between authentication and authorization?
  > authentication verify you are who you say you are
  > authorization verify that you are authorized to access what you’re trying to access

* Why is  has_secure_password a handy method?
  > `#has_secure_password` add methods to User model to work with password and generates *password_digest*

* What is the basic overview of how to authenticate a user with that method?


* What additional steps (on a high level) are needed to actually “remember” a user after they’ve closed the browser?
  > * create a *remember_token* virtual attribute for User model and *remember_digest* column in users table and saving that token to a permanent cookie in user’s browser. Reset on each new sign-in.
  > * on every page load that require authentication, frist check the user’s cookie *remember_token* against the database *remember_digest* to see if the user is already signed in.

* What is the Devise gem and why is it useful?