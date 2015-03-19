## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

####Part 1: Optimize PageSpeed Insights score for index.html

SHORTENING THE CRITICAL RENDERING PATH. The PageSpeed was improved to: Mobile 94 Desktop 95 after the following changes were applied.
1. "async" was added to the google analytics script;
2. media="print" was added to css/print.css to unblock critical rendering path;
3. change the perfmatters.js into inline script and minified the function logCRP;
4. inlined and minified style.css file;
5. moved the google font link to below the footer;
6. cam_be_like.jpg was compressed from 262Kb to 24KB;
7. mobilewebdev.jpg was compressed from 187Kb to 14KB;
8. pizzeria.jpg was compressed into pizzeria_tiny.jpg from 2.3Mb to 16Kb and pizzeria_tiny.jpg is being used on index.html



####Part 2: Optimize Frames per Second in pizza.html

The following changes were made to views/js/main.js:

1. change all querySelector to getElementById;
2. move some variables from for loop to ouside of loop in changePizzaSizes function;
3. create a new function CreatePizzas() to generate random pizzas and appends all the pizzas only once instead of 99 times in a for loop when the page loods ;
4. move document.body.scrollTop outside of the for loop in updatePositions function;
5. In addEventListener, loop through 32 (8 per row x 4 rows) times instead of 200 times;

