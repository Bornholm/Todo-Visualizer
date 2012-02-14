# Todo.txt JQuery Plugin

A quick & dirty vizualizer for **Todo.txt** file format, a great but simple way to create todo lists.

You can learn more [here](https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format) about the **Todo.txt** format.

This plugin has been tested with JQuery 1.7.1

# Example

See [here](http://bornholm.github.com/Todo-Visualizer/) for an interactive demo

# How to

Include the followings files in your HTML template

```html
<link rel="stylesheet" href="/path/to/todo.css"> <!-- Default Todo Style -->
<script type="text/javascript" src="/path/to/jquery.js"></script> <!-- Require JQuery ! -->
<script type="text/javascript" src="/path/to/jquery-todo.js"></script>  <!-- Plugin script -->
```

To create a new Todo, in your html template

```html
<div id="todo-container"></div> <!-- Todo List Container -->
<script type="text/javascript">

	$(document).ready(function(){

		$("#todo-container").todo({ 
			url : "/path/to/your/todo.txt"
		});
		
	});

</script>
```