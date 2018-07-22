# ActiveRecord Associations
`#activerecord`


* How does Rails normally know which table and foreign key to use when you have an association (e.g. `User.first.posts`)?

  - Rails use `has_many :posts` in User model to know the association with `posts` table

* When would you need to specify the `:class_name` option in an association?
  - When you want to associate a model with a model in a different namespace, you have to specify with `:class_name`

* What about the `:foreign_key`?
  - by default, Rails assumes that the column to hold the foreign key is the name of the association + suffix `_id`. The `:foreign_key` option lets you set the name of the foreign key.
    ```
    class Book < ApplicationRecord
      belongs_to :author
    end
    ``` 
    > Rails assumes default foreign key is `author_id` in `books` table

    ```
    class Book < ApplicationRecord
      belongs_to :author, class_name: "Binh",
                          foreign_key: "binh_id"
    end
    ```
    > Rails will look for foreign key `binh_id` in `binhs` table

* What about the `:source`?
    - Rails uses the name of the association in the through table to determine which *foreign key* and *table name* to reach out to. If it’s named anything irregular, you’ll use the `:source` option to specify which association actually points where we’d like to go. You can think of `:source` as being just like `:class_name` but for the associations in the “through table”.

* What is a polymorphic association and when would you use one?
  - When you want to use a model belongs to many different models
    ```
    # app/models/comments.rb
    class Comment < ApplicationRecord
      belongs_to :commentable, :polymorphic => true
    end

    # app/models/post.rb
    class Post < ApplicationRecord
      has_many :comments, :as => :commentable
    end

    # app/models/picture.rb
    class Picture < ApplicationRecord
      has_many :comments, :as => :commentable
    end
    ```

* What are two ways to use the association to create a new object instead of just calling `YourObject.new`? Why is this useful? Which method is preferred?
  - `association.yourobjects.new(...)` or `association.yourobject.create(...)`
  - or
    ```
    object = Object.new
    association.objects << object
    ```

* How do you automatically destroy all a User’s Post objects if that user is deleted?
How do you set up a self-association, like with Users following Users?

  - To automatic destroy association use `:dependent` option
    ```
    class Author < ApplicationRecord
      has_many :books, dependent: :destroy
    end
    ```
  - to setup self-association
    ```
    class Employee < ApplicationRecord
      belongs_to :manager, class_name: "User", foreign_key: "manager_id"
      has_many :subordinates, class_name: "User"
    end
    ```

