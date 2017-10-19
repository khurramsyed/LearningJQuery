

# Using JQuery 

## How can I use JQuery in my web page 

> Adding following line in your html , `Try to add this just before closing </body> tag`

```html 
<script src="jquery.min.js" /> 
```

Now that we have jQuery loaded, we need a place to put all the JavaScript code that we will be working on. Let's load our custom application.js file. Make sure `it's after` jquery.min.js, since we want to use that in our application.js file.

```html
<script src="application.js" /> 
```





## Selcting by element (Tag Name)

```javascript
	$("p") `Select all paragraphs` 
	$("h2") `Select all h2s`
	.
	.
```

## Selecting by css class
```javascript
	$(".mypara") `Select all elements where class name is mypara` 
	$(".mylabel") `Select all elements with class name mylabel`
```


## Selecting by id of an element
```javascript
	$("#mypara") `Select all elements where id is mypara` 
	$("#mylabel") `Select all elements where element id is mylabel`
```


## Select all the child tags of a type  of element 

In this case selector takes following form  ` $("#id > elementType")` , you can also select immediate childre using `$("#id").children()`



Please Ensure the Look at the API for jQuery all the time at [JQuery API Documentation](http://api.jquery.com)