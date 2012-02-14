# Todo.txt JQuery Plugin

A quick & dirty vizualizer for **Todo.txt** file format, a great but simple way to create todo lists.

You can learn more [here](https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format) about the **Todo.txt** format.

This plugin has been tested with JQuery 1.7.1


# How to

Include the followings files in your HTML template :

```html
<link rel="stylesheet" href="/path/to/todo.css"> <!-- Default Todo Style -->
<script type="text/javascript" src="/path/to/jquery.js"></script> <!-- Require JQuery ! -->
<script type="text/javascript" src="/path/to/jquery-todo.js"></script>  <!-- Plugin script -->
```

To create a new Todo :

```html
<div id="todo-container"></div> <!-- Todo List Container -->
<script type="text/javascript">

	$(document).ready(function(){

		var options = {
			url : "/path/to/your/todo.txt"
		};

		$("#todo-container").todo( options );

	});

</script>
```

## Options

 *url* : Todo.txt file url

 *headerAlias* : Columns headers alias

 _Example_

 ```javascript

 	var options = {

 		headerAlias : {

 			contexts : "Context(s)",
 			projects : "Project(s)",
 			text : "Task",
 			startDate : "Started",
 			priority : "Priority"

 		}

 	};
 	 
 ```

 *contentTransform* : Transform cells content

 _Example_

 ```javascript

 	var options = {

 		contentTransform : {
 			contexts : function(content) { return "Context : "+content; }
 		}

 	};
 	 
 ```



