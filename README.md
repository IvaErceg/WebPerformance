Part 1 : Mobile portfolio

How to run: Open index.html file in your web browser or go to https://ivaerceg.github.io/WebPerformance/.

Goal of this part of the project was to achieve score of 90 in Page Speed analysis (copy URL on designated place on https://developers.google.com/speed/pagespeed/insights/ and analyse).

The following optimizations were made on index.html:

1) Inlined and minfied all of the CSS into the head of the document and added the HTML media="print" attribute to the external style sheet link for print styles.

2) Used async and defer on analytics.js script.

3) Compressed and optimized all images so they are smaller in size(resized pizzeria image and changed it's src in index.html so it refers to smaller image in /img folder).

4) Removed custom font.


Part 2 : Cam's Pizzeria

How to run : Open views/pizza.html file in your web browser or go to https://ivaerceg.github.io/WebPerformance/views/pizza.html.

Goal was to acheive a frame rate of 60 FPS on the pizza.html and main.js files and also to resize pizzas in under 5s.

The following adjustments were made:

1. improving size slider
done by modifying resizePizzas function
Function determineDx was removed, instead function changePizzaSizes was modified so that it defines width attribute for corresponding size, and applies it to whole collection of pizzas in for loop. Changed selector querySelectorAll to getElementsByClassName, variables are defined outside of a loop so there is no repeated code.

2. getting to 60 FPS
done by modifying updatePizza function
Used getElementByClassName instead of querySelectorAll and defined variables outside of the loop so they are not constantly redefined. Changed number of moving pizzas on screen to  25 because there is never more visible then that. Used getElementByIf when selecting "movingPizzas1".