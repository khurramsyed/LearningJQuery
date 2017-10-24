



```javascript
$(document).ready(function() {
  //Create the click handler here
  $("#filters").on('click', '.on-sale', function(){
  		$('.on-sale').adClass('highlight');
  });
});
```


# Filtering Example.

Now let's make these filters work! Inside our event handler, find all .tour elements and filter() for only those that have a class of .on-sale. Add a class of highlight to only these filtered tours on click.
```html
<div id="all-tours">
  <h1>Guided Tours</h1>
  <ul>
    <li class="usa tour on-sale" data-discount="299">
      <h2>New York, New York</h2>
      <span class="details">$1,899 for 7 nights</span>
      <button class="book">Book Now</button>
    </li>
    <li class="europe tour on-sale" data-discount="176">
      <h2>Paris, France</h2>
      <span class="details">$2,299 for 7 nights</span>
      <button class="book">Book Now</button>
    </li>
    <li class="asia tour" data-discount="349">
      <h2>Tokyo, Japan</h2>
      <span class="details">$3,799 for 7 nights</span>
      <button class="book">Book Now</button>
    </li>
  </ul>
  <ul id="filters">
    <li><button class="on-sale">On Sale</button></li>
  </ul>
</div>
```


We will need following java script 

```javascript

$(document).ready(function() {
  $('#filters').on('click', '.on-sale', function() {
    $('.tour').filter('.on-sale').addClass('highlight');
  });
});
```