# Reading Keyboard Events and Inputs

> To read Keyboard events , use `keyup` , `keypress` and `keydown` events. 

```javascript
$(document).ready(function() {
  $('#nights').on('keyup', function() {
    var count = $(this).val();
    $('#nights-count').text(count);
  });
});
```

## Read value from input

In order to read value from input element , use elements val() function to set the value pass the value as parameter. By Default when you read the value it is read as string. If you want it as number you will need to put `+` before `$` sign
```javascript
 var countString = $('.className').val(); 

 var countNumber = +$('.className').val(); 
```






