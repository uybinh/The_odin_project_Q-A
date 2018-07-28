# Advanced Form

#rails #activerecord

* How do you prepopulate a dropdown menu with data?
  * use `select_tag`, `select`

* What is the difference between the #select_tag helper and the #select helper?
  * `select_tag` has to be used with `options_for_select`

* What format does the array you input to #options_for_select need to be in?
  * in [[key: value]] style

* Why would you need to use a nested form?
  * to submit data for different model

* What do you need to change in the model to allow nested forms to create new objects properly?
  * you have to add to the model method `accepts_nested_attributes_for`

* How do you whitelist the nested parameters properly in your controller?

* Why can’t you just delete something by leaving a form field (e.g. a checkbox) blank (unchecked)?