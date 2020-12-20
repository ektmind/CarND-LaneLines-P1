# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report




---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline has steps

	1. Read image
	2. Convert to gray
	3. Gaussian blur
	4. Canny edge detection
	5. Maksing the area
	6. Hough line detection
	7. draw lines the line
	
and I modified draw_line also

	1. calculate slope
	2. if slope is less than threshold (-0.3), I add it as left side and calculate average point
	   if slope is more than threshold (0.3), I add it as right side and calculate average point
	3. each side lines is extrapolate to the top and bottom. using mx + b equation



### 2. Identify potential shortcomings with your current pipeline


first of all, when the load color is bright similar as white, then canny edge detection is not working



### 3. Suggest possible improvements to your pipeline

along with gray covert, if RGB color is used also, then yellow line can be detected well
depens on the weather and road condition, if threshold can be adjust in edge detection, further improvements will be possible