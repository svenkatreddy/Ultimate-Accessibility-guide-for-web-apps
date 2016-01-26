# Ultimate-Accessibility-guide-for-web-apps
Ultimate Accessibility guide for web apps

## Basics
  Common misbelief is Web Accessibility is only for blind people. Accessibility is not just for **blind people**. It should include needs of people who have physical, hearing, cognitive disabilities. A good example of such is closed caption for deaf.

## Semantic tags
  For the starters, use `header`, `nav`, `article`, `section`, `aside`, and `footer` elements
  Whenever screenreader reads structural semantic tags, they add meaning to it. which makes more sense than a simple div container.
  
  Use `<strong>`, `<em>` instead of `<b>` , `<i>` tags. Use Header tags(`<h1>..<h6>`), paragraph (`<p>`) wherever permissible
  
## Tab Index
  * Tab index provides the tab order or reading order of content on the page. Without tabindex, usually screenreader follows DOM structure ( it is very important to define your DOM structure in the order you want it to read regardless to tabindex)
  
  ```html
  <a href="link1.html" tabindex=1>link 1</a>
  <a href="link2.html" tabindex=3>link 3</a>
  <a href="link3.html" tabindex=2>link 2</a>
  ```
  Screen Reader follows the tabindex and reads link1 followed by link 2 and then link 3
  
  Note: Avoid using `tabindex` for ordering because tabindex might cause confusion especially incase of single page web apps or dynamic portions.
  
  * use `tabindex=0` attribute for focussing elements which are not natively focusable (div, span, p). using tabindex=0 will keep element reading order same and doesnt increase or decrease priorty.
  ```html
  <div tabindex=0> Focussable and in reading order</div>
  ```
  
  * use `tabindex=-1` attribute for removing it from reading order but still focussable. Example: Popup wants to be focussed and read when it appears on the screen
  ```html
  <a tabindex=-1> Focussable and skipped in reading order</div>
  ```
  
## Input fields

* Use `for` attribute for `label` and associate with `input` ID

  ``` html
  <label for="fname">First Name</label>
  <input id="fname" name="fname" type="text" /> 
  ```
`for` should have same name as ID of the input field

* Use `title` attribute if there is no visual label

  ``` html
  <input title="Enter first name" type="text" />
  ```

* Use hidden `label` and `for` to associate with `input` fields

  ``` html
  <label for="fname" class="hidden">First name</label>
  <input id="fname" name="fname" type="text" />
  ````
class `hidden` should be defined in css to hide element visually

* Use `placeholder` text whereever it is permissible

  ```
  <input type="text" name="fname" placeholder="First name">
  ```
  
  
