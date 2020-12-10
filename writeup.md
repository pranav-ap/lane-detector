# Finding Lane Lines on the Road

Lane lines are a constant reference for where to steer the vehicle. One of the first things we would like to do while developing a self-driving car is to automatically detect lane lines. The goal of this project is build a lane detector to detect lane lines on the road.

<div align="center">
  <br>
  <img src="static\lane-detect.gif">
  <br>
  <br>
</div>

## Pipeline

- Convert image to grayscale
- Blur the image using Gaussian blur
- Use Canny edge detector to get edges of the image
- Blackout everything outside the region of interest
- Use Hough transform to detect lines in the edge-world image
- Draw the detected lines in the original image


## Reflections




