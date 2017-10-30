## Website Performance Optimization portfolio project
### Instructions

To view the portfolio website download all the files and open index.html in your browser.

To view the pizza website download all of the files and open views/pizza.html in your browser.

You can also view the site on github pages by using the links listed at the bottom.

## Optimizations to Pizza Site

1. Optimized the pizzarea picture which was huge (2.5MB) using the website http://www.jpegmini.com/main/shrink_photo which shrank it down to  around 32K.

2. Modified the code to put the styles inline instead of separate files (as instructed to do by PageSpeed Insights https://developers.google.com/speed/pagespeed/insights/).

3. Modified the code to calculate the number of pizzas needed to fill the webpage based on browser inner dimensions.

4. Moved the document.body request out of for loop in the changePizzaSizes and updatePositions functions. This prevents the browser from having to render the page every time the loop iterates.

5. Cached the needed DOM elements so that the brower isn't querying the DOM every time the for loops are iterated in the updatePositions and changePizzaSizes funcitons

6. Changed all instances of querySelector to the more efficient getElementById and getElementByClassName depending on whether a class or id is needed.

7. In the changePizzaSizes function I created an additional for loop for setting the element's width. This was done to group all of the DOM calls and the Rendering together in separate loops. This prevents the browser from having to render the page over and over in between setting the styles.


To view the portfolio site on github pages go to http://github.com/szelazny/frontend-nanodegree-mobile-portfolio/

To view the pizza site on github pages go to https://szelazny.github.io/frontend-nanodegree-mobile-portfolio/views/pizza.html


