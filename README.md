# rallio-todos

Use this doc for the app spec requirements. Begin by understanding the [Template section of the Functionality Requirements](https://github.com/marclundgren/rallio-todos#template).

If you have any questions about the requirements, this document, or running the ember application on your computer locally, let us know as soon as you can.

## Functionality Requirements

### Template

[Ember.js](https://emberjs.com/) uses a templating system called `htmlbars`, which is modeled after [Handlebars](http://handlebarsjs.com/). Check out their documentation for reference only, ignoring the javascript portion of handlebars.

Handlebars and htmlbars are templating systems that produce raw html markup. In this challenge, we can provide the end result desired [html markup](https://github.com/rallio/rallio-todos/blob/master/index-static.html). Your goal is to write use ember.js to write the dynamic templates and javascript controllers to "wire up" the UI.

You'll note a few things in the template:
* There is no styling, that's for you to add 😁
* There is a header, main section and footer
* The header has an input for adding a new todo
* Inside the main section a list `ul` of todos `li` exist
* Each `li` todo has a conditional `completed` class name
* Each `li` todo has a label (e.g. Buy a unicorn)
* (optional) the footer has 3 selectable filters: "All", "Active", "Completed"
* (optional) the footer has a "clear all completed" button

### (required) No todos
When there are no todos, the list of todos `<main></main>` and (optional) filters `<footer></footer>` should not be displayed. IOW, only display these elements when there is at least one todo.

### (required) New todo
New todos are entered in the input at the top of the app. When text is present inside the input a button should appear. Pressing the button creates the todo, appends it to the todo list, and clears the input. (optional) Pressing Enter when the input is focuses behaves the same way by adding the todo and clearing the input. (optional) Before creating the todo, `.trim()` the input. (optional) Check that it's not empty before creating a new todo.

### (optional) New todo focus
The input element should be focused when the page is loaded, preferably by using the autofocus input attribute.

### (required) clicking a todo's checkbox
Clicking the checkbox marks the todo as complete by updating its completed value and toggling the class completed on its parent `<li>`. (optional) clicking the checkbox again will toggle the completed task back to uncompleted.

### (optional) Counter
Displays the number of active todos in a pluralized form. Make sure the number is wrapped by a `<strong>` tag. Also make sure to pluralize the item word correctly: 0 items, 1 item, 2 items. Example: 2 items left

### (optional) Clear completed button
Removes completed todos when clicked. (optional) Should be hidden when there are no completed todos.

### (optional) All, Active, Completed Filters
"All" should be active by default and will display all todos, regardless of their "completed" status. Selecting the "Active" filter will display only todo items that have `completed === false`. Selecting the "Completed" filter will display only todo items that have `completed === true`.

### (required) UI layout

Structure the UI to look something like the following example. Structure and layout are much more important than the "look-and-feel" or "skin". Focus on getting elements to align properly first before making it look 💄. Consider todos with a very long body, be careful these types of todos maintain the integrity of the structure.

![example ui](https://user-images.githubusercontent.com/1154834/51417110-69917a80-1b31-11e9-8de3-f83f4ab924b8.png)

## Ember.js Concepts
Routes
    In Ember, the state of an application is represented by a URL. Each URL has a corresponding route object that controls what is visible to the user.

Models
    Every route has an associated model, containing the data associated with the current state of the application.[20] While one can use jQuery to load JSON objects from a server and use those objects as models, most applications use a model library such as Ember Data to handle this.

Templates
    Templates are used to build the application's HTML and are written with the HTMLBars templating language. (HTMLBars is a variation of Handlebars that builds DOM elements rather than a String.)[21]

Components
    A component is a custom HTML tag. Behavior is implemented using JavaScript and its appearance is defined using HTMLBars templates. Components "own" their data. They can also be nested and can communicate with their parent components through actions (events). Other component libraries such as Polymer can also be used with Ember.

## Ember.js Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with npm)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone marclundgren/rallio-todos` this repository
* `cd rallio-todos`
* `npm install`

## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

## Further Reading / Useful Links
* [single-page-application](https://en.wikipedia.org/wiki/Single-page_application)
* [ember.js wikipedia](https://en.wikipedia.org/wiki/Ember.js)
* [ember.js](https://emberjs.com/)
* [5 essential ember concepts](https://emberigniter.com/5-essential-ember-concepts/)
* [handlebars](http://handlebarsjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
