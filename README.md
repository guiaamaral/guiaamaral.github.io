# Website Performance Optimization portfolio project
#### Optimize PageSpeed Insights score for index.html
1. Minimized and inlined styles from `style.css`
2. Define `media="print"` for `print.css`
3. Remove Google Font
4. Moved all JS to the end of `index.html` file and define to them `async`
5. Minimized `perfmatters.js`
6. Optimized and compressed all images
7. Create reduced and compressed `pizzeria-small.jpg` from `pizzeria.jpg`

Now the score from PageSpeed Insights is:
- Mobile: 94
- Desktop: 95

#### Optimize Frames per Second in pizza.html
1. In `main.js` on `changePizzaSizes()` function I remove the class `.randomPizzaContainer` selector and declared two variables outside the `for` loop using the first size as model and then assigned the new size inside the loop
2. In `main.js` on `updatePositions()` function I created an array to calculate and store five numbers outside the `for` loop and then assigned them inside the loop. Besides this I reduced the amount of pizza elements generated from 200 to 30 that is still sufficiently to fill the screen and added a scroll event listener with requestAnimationFrame on updatePositions which optimizes the animations doing a single reflow and repaint cycle.