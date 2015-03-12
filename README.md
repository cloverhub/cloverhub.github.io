## Website Performance Optimization portfolio project

[View project hosted on GitHub Pages](http://cloverhub.github.io/)

### Tested Results

#### PageSpeed
* Desktop 97/100
* Mobile 95/100

#### Cam's Pizzeria JavaScript Performance
* Average time to generate last 10 frames on scroll: ~0.27ms
* Time to resize pizzas: 0.6130000001576263ms

### Optimizations Made

#### HTML/CSS
* Added media attribute to print css file to remove from critical path
* Minified CSS file and placed inline in html file
* Removed call to Google font
* Changed analytics.js to load async to remove from critical path
* Minified inline JavaScript
* Moved scripts to bottom of html

#### Images
* Made a separate 100px thumbnail for pizzeria image
* Optimized all locally-hosted images in Photoshop web optimized mode
* Further compressed images using compressnow.com after Google complained images could still be optimized

#### Pizza Page JavaScript (main.js)
* Use dynamic browser window size to reduce pizzas generated to a minimum
* Simplified FOR loops wherever possible so calculations can be made outside of loop to reduce loop payload
* Changed window scroll position so it is stored outside of the loop and avoids repeatedly calculating
* Replaced document.querySelectorAll with document.getElementsByClassName where possible to boost performance
* Created an array of five phases of the pizza scroll so that the array can be accessed from the FOR loop rather than use excessive calculations
* Minified JavaScript into separate min file