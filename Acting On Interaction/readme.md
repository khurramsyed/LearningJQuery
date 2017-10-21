# Acting on Interaction

First thing that you will need to know is that , you can only execute this code once document is ready. So you will need to write whole code inside  ` $(document).ready(callBack_Function);` function. i.e. in your applciation.js script.

your code will be like so

```javascript

	$(document).ready(function(){
			// You code goes here.
	});

```


Next first thing you will need to do is to find the element to which you need to attach event handing logic. you do this by calling `on()` function of dom element. For that you need to traverse or search the element and attach handler to it using `on('event name', callback)` method. Lets see the code example here for exmple you want to delete the button with class `button` and  add details for booking when button is clicked. 

```javascript

		$('.button').on('click', function() { // search the button with class , on click add handler function.
		  var message = $('<span>Call 1-555-jquery-air to book this tour</span>');
		  $('.usa').append(message);
		  $('.button').remove();
		});
```

or if its any button element.
```javascript

	$(document).ready(function(){
		$('button').on('click', function() {
		  var message = $('<span>Call 1-555-jquery-air to book this tour</span>');
		  $('.usa').append(message);
		  $('button').remove();
		});
	});
```




### Identifying the soruce element for event.
You can use `$(this)` inside element handler function to identify source element. For example if you want to remove the button which was clicked. Your code will look like this.

```javascript
	$(document).ready(function(){
		$('button').on('click', function() {
		  $(this).remove();
		});
	});
```




