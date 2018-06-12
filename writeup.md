# **Finding Lane Lines on the Road** 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.
Pipeline includes these 4 parts:
* Grayscale the image
* Apply Gaussian blurring
* Canny edge detection
* Hough Transfom to get lines and draw it

I modify the draw lines by 
* pick the longest segment from Hough Transform result for left and right side
* Expolate the lines until intersect with region of interest.


![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

Potential shortcoming is in my draw_lines() I only pick the current longest segments. This does not work
when the leans is curve. I should improve temporal (history) data to do time-wise averaging or filtering.



### 3. Suggest possible improvements to your pipeline

* Implement a historical filter to buffer previous lanes, and do smoothing on it.

