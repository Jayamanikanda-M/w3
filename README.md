# WORKSHOP 3 – Canny Edge Detection
# Aim
To implement the Canny Edge Detection algorithm on a sample image using Python and OpenCV, obtain the edges present in the image, analyze the detected edges, and study the effect of different parameter settings on the output.

# Algorithm
The Canny Edge Detection algorithm is performed in the following steps:

Convert the image to grayscale
The input image is converted from RGB/BGR to grayscale to simplify edge detection. Noise Reduction

A Gaussian Blur is applied to the grayscale image to reduce noise and unwanted details. Gradient Calculation

The intensity gradients in the horizontal and vertical directions are calculated to identify areas with significant intensity changes. Non-Maximum Suppression

Non-edge pixels are suppressed, making the detected edges thin and well-defined. Double Thresholding

Two threshold values, minVal and maxVal, are used to classify pixels as:

Strong edges Weak edges Non-edges Edge Tracking by Hysteresis

Weak edges connected to strong edges are retained, while isolated weak edges are removed.

# Program
Devloped by JAYAMANIKANDA M REGNO:-212225230113 
Python Code
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('Dhanush.jpg',cv2.IMREAD_GRAYSCALE)
blurred =cv2.GaussianBlur(img, (5,5),0)
edges = cv2.Canny(blurred, 50, 150)
plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```
# Output
<img width="955" height="535" alt="image" src="https://github.com/user-attachments/assets/411ab691-7e36-4bfb-94da-3bed25431620" />

The final image contains the detected edges.

# Result
The Canny Edge Detection algorithm was successfully implemented using Python and OpenCV. The algorithm detected significant edges and boundaries in the sample image. Different threshold values were 
tested, and it was observed that lower thresholds detect more edges including fine details and noise, whereas higher thresholds detect fewer and stronger edges.

Thus, Canny Edge Detection is effective for extracting meaningful edges from images while reducing the influence of noise.







..








..
