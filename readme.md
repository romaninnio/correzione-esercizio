# Javascript Slideshow

This is an infinite loop Javascript exercise for Picture Slideshow.

Here’s how the JavaScript look:

```
var myImage = document.getElementById("slideshow-container");
var images = ["img/1.png", "img/2.png", "img/3.png", "img/4.png"];
var imageIndex = 0;

function imagechange() {
myImage.setAttribute("src", images[imageIndex]);
if (imageIndex < 3) {
imageIndex++;
} else {
imageIndex = 0;
}
}

var interval = setInterval(imagechange, 4000);
myImage.onclick = function() {
clearInterval(interval);
}
```

Let’s break down what’s happening here.

First we’re setting a variable "myImage" to keep track of the slides.

Next we're creating an array and populate it with all the images that we are going to be using.

After we're setting the initial index of the array to 0 and making this index increase by 1, reach the number of 3 and turn back to his initial value each time the function runs.

We’re finally setting an interval to run this function every four seconds (expressed as 4000 ms).
