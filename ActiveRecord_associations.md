# ActiveRecord Associations
`#activerecord`


* How does Rails normally know which table and foreign key to use when you have an association (e.g. `User.first.posts`)?

  Rails use `has_many :posts` in User model to know the association with `posts` table

* When would you need to specify the `:class_name` option in an association?
  When you want to associate a model with a model in a different namespace, you have to specify with `:class_name`

* What about the `:foreign_key`?
  by default, Rails assumes that the column to hold the foreign key is the name of the association + suffix `_id`. The `:foreign_key` option lets you set the name of the foreign key.
  ```
  class Book < ApplicationRecord
    belongs_to :author, counter_cache: :count_of_books
  end
  ```

* What about the `:source`?


* What is a polymorphic association and when would you use one?
* What are two ways to use the association to create a new object instead of just calling `YourObject.new`? Why is this useful? Which method is preferred?
* How do you automatically destroy all a User’s Post objects if that user is deleted?
How do you set up a self-association, like with Users following Users?