

#Select an element

*jQuery("elementTagName")* eg jQuery("document") or jQuery("h1") or jQuery("span")

There is short form for jQuery() function , which is $(), you can write above as following:
$("document"), $("h1") and so on.

To select contents on element for example below use .text() function of element.
<h1>Welcome to JQuery</h1>

** $("h1").text() **



##To Modify content of an element 

Search the element and then use  text("Value to Set");

e.g. for above  

```jQuery
$("h1").text("Learnt first part of jQuery");
```

###When can I start using jQuery


use $(document).read(callback_Fucntion) .

For example.

```jQuery
$(document).ready( function(){
    $("span").text("$100");
});
```