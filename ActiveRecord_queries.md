# Active Record queries

* What is an ActiveRecord::Relation?
  * Relations looking like arrays but they’ve got more going on
  * ActiveRecord queries usually return Relations 

* What does Lazy Evaluation mean?
  * Relations only get executed when it becomes absolutely necessary to know what’s inside them.

* How do you make a relation evaluate into an array?
  * user `#to_a` method

* How do you check whether a database already contains a record?
  * use `#exist?`, `#any`?

* Why is “find_by” useful and how is it used?
  * `#find_by` let you build your own finder method
  * `#find_by` finds the first record matching some conditions
(it’s an alternative to using `#where` which you have to add another method lide `#first`, `#take` to pull the result out of the return array)
  ```
  User.find_by(name: “Binh”);
  User.find_by(:name => “Uy Binh”)
  User.where(:name => “Binh”).first
  User.where(name: “Binh”)[0]
  ```

* What’s the difference between what’s returned using a  `#where` query and a  `#find` query?
  * `#find` return an actual record while `#where` return a relation
  * `#find` return a single instance of a model (also ‘take’ method)
  * `#where` return an instance of ActiveRecord::Relation (also ‘group’ method)

* How do you join tables together in Rails?
  * ActiveRecord provides two finder methods `#joins` and `#left_outer_joins`

* When can you use symbols / hashes and when do you need to use explicit strings for query parameters?

* What are Scopes and why are they useful?
  * Scoping allows you to sepcify commonly-used queries which can be referenced as method calls on the association objects or models.

* What needs to happen for a class method to act like a scope?

[ActiveRecord queries lesson](https://www.theodinproject.com/courses/ruby-on-rails/lessons/active-record-queries)




