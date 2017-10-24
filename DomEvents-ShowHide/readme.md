# Hide and Display elements using either slideDown , slideToggle or slideUp Methods.

For Following HTML excerpt:

Display elements using slideDown function on '.photos' element.

```html
      <div id="tour">
        <h2>Paris, France Tour</h2>
        <p>$2,499 for 7 Nights</p>
        <button>See photos from our last tour</button>
        <ul class="photos">
          <li>
            <img src="/assets/photos/paris1.jpg">
            <span>Arc de Triomphe</span>
          </li>
          <li>
            <img src="/assets/photos/paris2.jpg">
            <span>The Eiffel Tower</span>
          </li>
          <li>
            <img src="/assets/photos/paris3.jpg">
            <span>Notre Dame de Paris</span>
          </li>
        </ul>
      </div>
```

Description: Display the matched elements with a sliding motion.


```javascript
      $(document).ready(function() {
        $('#tour').on('click', 'button', function() {
          $(this).closest('#tour').find('.photos').slideDown();
        });
      });
```

## Show and Hide with same code 

```javascript
You can use slideToggle to show and hide.

      $(document).ready(function() { 
        $("#tour").on('click', 'button', function() { 
          $('.photos').slideToggle();
        });
      });
```
## SlideToggle

Inside our new mouseenter event handler, call the slideToggle() method on the span tag within the picture description. You'll need to traverse down from the current element, $(this), and then find() the span tag.

```javascript 
$(document).ready(function() {
  $('#tour').on('click', 'button', function() {
    $('.photos').slideToggle();
  });
  $('.photos').on('mouseenter', 'li', function() {
    $(this).find('span').slideToggle();
  });
});
```




