# Finding First Element matching criteria in hierarchy..

For Example if I have following html 


```html
<div id="tours">
  <h1>Guided Tours</h1>
  <ul>
    <li class="usa tour">
      <h2>New York, New York</h2>
      <span class="details">$1,899 for 7 nights</span>
      <div>
        <button class="book">Book Now</button>
      </div>
    </li>
    <li class="europe tour">
      <h2>Paris, France</h2>
      <span class="details">$2,299 for 7 nights</span>
      <div>
        <button class="book">Book Now</button>
      </div>
    </li>
    <li class="asia tour">
      <h2>Tokyo, Japan</h2>
      <span class="details">$3,799 for 7 nights</span>
      <div>
        <button class="book">Book Now</button>
      </div>
    </li>
  </ul>
</div>
```

You want to add a label after div containing the button that was click. Now we have two issues:

 **Find the element that originated the issue ** 

 **Find correct place where to add the new message. ** 
