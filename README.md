# Website Performance Optimization portfolio project

#### Instructions

To run the portfolio website download the repository and open index.html in your browser. To view the pizza website access the project "Cam's Pizzeria" listed on portfolio homepage or open views/pizza.html.

Alternatively, you can view online just [clicking here](https://guiaamaral.github.io/udacity-mobile-portfolio/).

#### Optimize PageSpeed Insights score for index.html
1. Minimized and inlined styles from `style.css`
2. Define `media="print"` for `print.css`
3. Remove Google Font
4. Moved all JS to the end of `index.html` file and define to them `async`
5. Minimized `perfmatters.js`
6. Optimized and compressed all images
7. Create reduced and compressed `pizzeria-small.jpg` from `pizzeria.jpg`

Now the score from PageSpeed Insights is:
- Mobile: 93
- Desktop: 95

#### Optimize Frames per Second in pizza.html
Changes made on `main.js`
1. Changed `querySelector` to `getElementsById` on `windowWidth`
2. Created a `randomPizzaContainer` var to select DOM elements outside the `changePizzaSizes()` function
3. Changed `querySelectorAll` to `getElementsByClassName` on new `randomPizzaContainer` var
4. Removed `dx` and `newwidth` vars from `changePizzaSizes()` function and `for` loop
5. Created a `pizzaSize` var with repeated query to select a DOM element and change `querySelector` to `getElementById`
6. Created an array on `updatePositions()` function to calculate and store five numbers outside the `for` loop and then assign them inside the loop
7. Changed `querySelectorAll` to `getElementsByClassName` on `item` var
8. Reduced the amount of pizza elements generated from 200 to 30 that is still sufficiently to fill the screen
9. Changed `querySelector` to `getElementsById` on loop that move the background pizzas
10. Added a scroll event listener with `requestAnimationFrame` on `updatePositions` which optimizes the animations doing a single reflow and repaint cycle