

#Select an element

*jQuery("elementTagName")* eg jQuery("document") or jQuery("h1") or jQuery("span")

There is short form for jQuery() function , which is $(), you can write above as following:
$("document"), $("h1") and so on.

To select contents on element for example below use .text() function of element.
<h1>Welcome to JQuery</h1>

``` `$("h1").text()` ``` 



## To Modify content of an element 

Search the element and then use  text("Value to Set");

e.g. for above  

```javascript
$("h1").text("Learnt first part of jQuery");
```

###When can I start using jQuery


use $(document).ready(callback_Fucntion).

> This means that only start jQuery Processing once document is comletely loaded and ready to be processed.

For example.

```javascript
$(document).ready( function(){
    $("span").text("$100");
});
```