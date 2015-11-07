# Ultimate-Accessibility-guide-for-web-apps
Ultimate Accessibility guide for web apps

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
