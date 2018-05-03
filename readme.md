# Javascript Slideshow

This is an infinite loop Javascript exercise for Picture Slideshow.

Here’s how the JavaScript look:

```
var imageIndex = 0;

        function imagechange() {
            $(".image").addClass("invisible");
            $(".image").eq(imageIndex).removeClass("invisible");
            

            if (imageIndex < 3) {
                imageIndex++;
            } else {
                imageIndex = 0;
            }
        }

        setInterval(imagechange, 1800);
```

Let’s break down what’s happening here.

To add a fade effect to the Slideshow we're initially add invisible class to every ".image" Node to subsequently remove it from the node with the current ".image" index.

We're setting the initial index of the ".image" NodeList object to 0 and making this index increase by 1, reach the number of 3 and turn back to his initial value each time the function runs.

We’re finally setting an interval to run this function every 1,8 seconds (expressed as 1800 ms).