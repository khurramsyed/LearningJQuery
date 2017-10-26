# Ajax


## Sending Data 

you can use `$.ajax(url,{success : callback}, jsonObject );`  , where first object is the url which you are invoking , second one is json object showing what should happen in case of success
like so { success: callback } and third one is json response data.

For static content you can send data like so:

```javascript
 $.ajax('/photos.html', {
      success: function(response) {
        $('.photos').html(response).fadeIn();
      },
      data :{ location : 'london'}
    });
```

In order to get data from form field dynamically you can send it like below. where `$('#tour').data("location")` dynamically selects the value from elements of form.


```javascript
 $.ajax('/photos.html', {
      success: function(response) {
        $('.photos').html(response).fadeIn();
      },
      data :{ location : $('#tour').data("location")}
    });
```


## Handling Error Scenario

For Error scenarior $.ajax() provides another json object  like so.

```javascript
	 error: function() {
        $('.photos').html('<li>There was a problem fetching the latest photos. Please try again.</li>');
      }
``` 

Since different browsers have different timeout settings , so for consistent customer experience it is important to mention timemout , So Your code will look something like this :

```javascript
$(document).ready(function() {
  var el = $("#tour");
  el.on("click", "button", function() {
    $.ajax('/photos.html', {
      data: {location: el.data('location')},
      success: function(response) {
        $('.photos').html(response).fadeIn();
      },
      error: function() {
        $('.photos').html('<li>There was a problem fetching the latest photos. Please try again.</li>');
      },
      timeout: 3000
    });
  });
});
```



If you want to do something before sending ajax data , you will need to do that in function for beforeSend object. similary if you want to do somethinkg as soon as data is received you can do that in complete object as below
```javascript

$(document).ready(function() {
  $("#tour").on("click", "button", function() {
    $.ajax('/photos.html', {
      success: function(response) {
        $('.photos').html(response).fadeIn();
      },
      error: function() {
        $('.photos').html('<li>There was a problem fetching the latest photos. Please try again.</li>');
      },
      timeout: 3000,
      beforeSend: function(){
      	$('#tour').addClass('is-fetching');
      },
      complete: function(){
      	$('#tour').removeClass('is-fetching');
      }
    });
  });
});

```