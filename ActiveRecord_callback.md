# ACTIVE RECORD CALLBACKS

#learning #odin_project

1. What is a callback used for?
  * is a method that get called at a certain moments of an object's life circle

2. What are the major lifecycle stages of an Active Record object?
  * save
  * create
  * delete
  * update
  * validate
  * load

3. How do you build an “around” callback?
    ```
    class User < ApplicationRecord
      around_save :show_messages  
      def show_messages
        puts "Before stage/action"
        yield
        puts "After stage/action"
      end
    end
    ```
4. How do you specify a particular action to run a callback for?
    ```
    class User < ApplicationRecord
      before_validation :downcase_name, on: :create
      def downcase_name
        name.downcase!
      end
    end
    ```

