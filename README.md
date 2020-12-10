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

<p float="left">
  <img src="test_images\solidWhiteCurve.jpg" width="48%" />
  <img src="test_images_output\Processed_solidWhiteCurve.jpg" width="48%" />
</p>

## Future work

- I have not supported different lighting conditions. Any dark images would probably screw up the lane predictions.
- The Hough transform is currently only looking for straight lines. Unless you live on a chess board, this is not good enough.
- Some roads may not have lane lines at regualr intervals. I need to sort this out.

## References

- [Wikipedia: Canny Edge Detector](https://en.wikipedia.org/wiki/Canny_edge_detector)
- [Hough Transform](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_houghlines/py_houghlines.html)
- [Wikipedia: Hough Transform](https://en.wikipedia.org/wiki/Hough_transform)
- [Canny Edge Detection Step by Step](https://towardsdatascience.com/canny-edge-detection-step-by-step-in-python-computer-vision-b49c3a2d8123)
