# default Link Behavior

By Default event is propagated to the parent and grand parent and then reaches to the top elemnt i.e the document. which means if you click say a link `#` then whole page will jump to the top of page , which is not what you want.

to preven the event from bubbling up to parent , you can create event handler function with event as paramenter and then stopPropagation of event.

```
event.stopPropagation
```

> `#` is a special case where page jumps to top , if you have multiple such links at bottom of page then it will jump to top of page to stop that you can use `event.preventDefault()`

See following example:


```javascript
$(document).ready(function() {
  $('.see-photos').on('click', function(event) {
    event.stopPropagation();
    event.preventDefault();
    $(this).closest('.tour').find('.photos').slideToggle();
  });
  $('.tour').on('click', function() {
    alert('This event handler should not be called.');
  });
});
```