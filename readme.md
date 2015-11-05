# Initial setup

- Fork this git repository 
- Read carefully this document and implement the 3 new requirements 
- Reply the e-mail you received from HR including a hyperlink to your git repository

# New requirements to be implemented by the candidate

- Improve the user experience using your best judgment. Impress us changing the font, including images/glyphicons, changing the colors using [this pallete](http://www.colourlovers.com/palette/92095/Giant_Goldfish)
- Include the date and time the todo was created/edited
- There is bug in the application functionality, validate the application against the specification and fix the bug. 

# Application Specification

We have created this short spec to help you create awesome and consistent todo apps. Make sure to not only read it, but also understand.

## Structure

### Code

Make sure to follow these:

- Follow our [code style](codestyle.md).
- Use double-quotes in HTML and single-quotes in JS and CSS.
- Apps should be written without any preprocessors (Sass/CoffeeScript/..).
- We require apps to work in every browser we support (latest: Chrome, Firefox, Opera, Safari, IE9).

## Functionality

### No todos

When there are no todos, `#main` and `#footer` should be hidden.

### New todo

New todos are entered in the input at the bottom of the app. The input element should be focused when the page is loaded preferably using the `autofocus` input attribute. Pressing Enter creates the todo, appends it to the todo list and clears the input. Make sure to `.trim()` the input and then check that it's not empty before creating a new todo. The application should not allow a todo with the same name an existing one.

### Mark all as complete

This checkbox toggles all the todos to the same state as itself. Make sure to clear the checked state after the "Clear completed" button is clicked. The "Mark all as complete" checkbox should also be updated when single todo items are checked/unchecked. Eg. When all the todos are checked it should also get checked.

### Item

A todo item has three possible interactions:

1. Clicking the checkbox marks the todo as complete by updating its `completed` value and toggling the class `completed` on its parent `<li>`

2. Double-clicking the `<label>` activates editing mode, by toggling the `.editing` class on its `<li>`

3. Hovering over the todo shows the remove button (`.destroy`)

### Editing

When editing mode is activated it will hide the other controls and bring forward an input that contains the todo title, which should be focused (`.focus()`). The edit should be saved on both blur and enter, and the `editing` class should be removed. Make sure to `.trim()` the input and then check that it's not empty. If it's empty the todo should instead be destroyed. If escape is pressed during the edit, the edit state should be left and any changes be discarded.

### Counter

Displays the number of active todos in a pluralized form. Make sure the number is wrapped by a `<strong>` tag. Also make sure to pluralize the `item` word correctly: `0 items`, `1 item`, `2 items`. Example: **2** items left

### Clear completed button

Removes completed todos when clicked. Should be hidden when there are no completed todos.
