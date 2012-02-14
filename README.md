Todo.txt - JQuery Plugin
======================

A quick & dirty vizualizer for **Todo.txt** file format, a great but simple way to create todo lists.

You can learn more [here](https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format) about the **Todo.txt** format.

This plugin has been tested with JQuery 1.7.1

Demo
----

Check the demo [here](http://bornholm.github.com/Todo-Visualizer)

How to
------

Include the followings files in your HTML template :

	<link rel="stylesheet" href="/path/to/todo.css"> <!-- Default Todo Style -->
	<script type="text/javascript" src="/path/to/jquery.js"></script> <!-- Require JQuery ! -->
	<script type="text/javascript" src="/path/to/jquery-todo.js"></script>  <!-- Plugin script -->

To create a new Todo :

	<div id="todo-container"></div> <!-- Todo List Container -->
	<script type="text/javascript">
		$(document).ready(function(){
			var options = {
				url : "/path/to/your/todo.txt"
			};
			$("#todo-container").todo( options );
		});
	</script>

Options
-------

**url** : Todo.txt file url

**local** : String to use as source *( \n is the line separator )*

**headerAlias** : Columns headers alias
 
*Example*
 
	var options = {
 		headerAlias : {
 			contexts : "Context(s)",
 			projects : "Project(s)",
 			text : "Task",
 			startDate : "Started",
 			priority : "Priority"
 		}
 	};
	
**contentTransform** : Transform cells content

*Example*

	var options = {
 		contentTransform : {
 			contexts : function(content) { return "Context : "+content; }
 		}
 	};



