* What are selectors?
  > patterns to select the elements you want to style

* In general, how specific should you be when targeting elements using selectors?
  > The more general the best
  > but it's best to lest than 3

* What’s the difference between using `%`, `em` and `rem` to specify sizes?
  > `%` in relative to the size of parent
  > `em` in relative to the font size of parent
  > `rem` in relative to the font size of root element

* How do you select an element inside another element?
  > To select an element in side an element we use `general decendent` (`div p`) combinator or `direct child` (`div > p`) combinator selectors

* How can you shorten up a long batch of CSS that’s doing the same thing to many different elements by putting them all in one line?
  > we use group the selectors together

* How do you target the immediate child of an element?
  > we use direct child combinator

* How do you target a class inside a class?
  > we use direct child combinator, or general decendent

* How do you target a class inside an ID?


* How would you target “all the links inside li elements that have the class bunny which are inside the unordered list with the id things-that-hop”?
  > `.bunny a { ... }

* What are the three ways to include CSS in your project?
  > use inline css
  > use `<style>` tag
  > use link file with `<link>`

* How do you import an external stylesheet?

* What is the browser’s default stylesheet?

* What is a “CSS Reset” file and why is it helpful?
  > CSS reset will reset all the default style of the browser default style sheet

* Which stylesheet has preference if you import multiple ones and there are overlapping styles?
  > The last style rule will be applied

* What is the order of priority of selectors (e.g. if you specify that the `<body>` has color black but `<h1>` tags have the color blue but class main-title has the color red, which will be used by `<body style="color:yellow"><h1 class="main-title" style="color:green">Howdy!</h1><body>?`)
  > black, blue, red, yellow, green