* What is the DOM?

* How do elements get placed in the DOM by default?
  elements places in normal flow

* How can you override element positioning using the position attribute?
  > you can use position static (default), ralative, absolute, fixed

* When are you able to use the top left right and bottom attributes?
  > when you declare position with properties other than static (ralative, absolute, fixed)

* What is the difference between float and position?
  > while floating is used for positioning purposes, floating isn't a "type o positioning"
  > floating is floating
  > floating does take element out of the "normal flow"

* Which element acts as the parent for a floated element?
  > the closest parent which has position: relative

* What is the difference between floating right and floating left?

* If you have a bunch of elements floated next to each other and you make the browser narrower, what happens?

* What’s the practical difference between relative and absolute positioning?
  > with relative the element still in the normal flow
  > with absolute the element is out of normal flow

* Which element acts as the parent for an absolutely or relatively positioned element?
  > the closest parent with position: relative

* How would you set up a grid of 20x20 boxes on the page using floats? Using lists?
  > use float left
  > use li with display: inline-block

* What are negative margins useful for?
  > for special decoration