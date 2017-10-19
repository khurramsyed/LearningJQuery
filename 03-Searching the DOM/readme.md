
To do list 
- [x] Searching the Dom
- [ ] Traversing the Dom

# Searching the DOM
## Using Descendent Selector

You can do this using `$("#id childTagName") ` for example 
```javascript 
$("#vacations li"); 
```

> Will select all the list items inside element with id vacations including grand children or underneath as well.

## Direct child selector
In order to select direct children of particular  type use `$(#id > childElementType)` for example

```javascript 
$("#vacations > li") ;
```

## Selecting Multiple items at a time

To select multiple items each by different selector you can use something as follows.

```javascript 
	$(".aClass, #anId");
```

or 
```javascript
	$(".asia, .sale");
```


To Select First Item in the list 

```javascript 
	$("#id li-first");
```


To Select Last Item in the list 
```javascript 
	$("#id li:last");
```

>you can also play with `$("#id > li:odd");` , `$("#id > li:last");`  and `$("#id li:even")` and so on.



# Traversing the Dom

