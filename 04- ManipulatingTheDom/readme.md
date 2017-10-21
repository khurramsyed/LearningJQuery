

# Create a node and adding to dom in correct location.

Using `$('<any_html_tag>Content </any_html_tag>)` creates the dom node but does not add to the dom. You will need to use `appendTo(), prependTo() , isertAfter() or insertBefore ()` methods to add dom to correct location.



```javascript
var newDomElement = $('<p>My Content</p>'); // Create Dom Element
$("#mySelectedElement").

```


> $("#mySelectedElement").appendTo(newDomElement) adds newDomElement as last child to element with id "mySelectedElement".
> $("#mySelectedElement").prependTO(newDomElement) adds newDomElement as first child to element with "mySelectedElement".

> $("#mySelectedElement").insertAfter(newDomElement) adds newDomElement as after element with id "mySelectedElement".
> $("#mySelectedElement").insertBefore(newDomElement) adds newDomElement as before element with id "mySelectedElement".



# Remove an element from dom.

Simply Search/traverse  an element and the remove it, using `remove()`.

```javascript/
$(".element").remove()
```


Use Following Link ot Learn More most of this is from [Code School](http://try.jquery.com)