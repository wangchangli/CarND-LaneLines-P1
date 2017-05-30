**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then applied Canny transform to the images, 
after that I defined a polygon to mask the images, then run Hough on edge detected images and drawn the lines on them,
finally, I drawn the lines on the origin images.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by calculating the average slope 
and the average point of the lines for each side lane. Then I can get a certain line from the given slope and point. 
Then I draw the lines, and extrapolate them to the top and bottom of the lane.


### 2. Identify potential shortcomings with your current pipeline

It is not precise enough to use average slope and point to calculate a line. 

It is not robust to deal the curve lane.

### 3. Suggest possible improvements to your pipeline

Using linear regression is a better solution for drawing line?
