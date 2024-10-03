# EDGE-DETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load a image using imread() from cv2 module.

### Step 3:
Convert the image to grayscale

### Step 4:
Using Sobel operator from cv2,detect the edges of the image.

### Step 5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed By: Bejin.B
Register No: 212222230021
```
```python
# Import necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('img3.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
### ORIGINAL IMAGE 

![image](https://github.com/user-attachments/assets/1f77cceb-6783-441d-8ad9-f1805c48be15)



### SOBEL EDGE DETECTOR
```python
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
```
![image](https://github.com/user-attachments/assets/d9f730b6-d9fc-41db-80fa-c3b7710ea59f)


### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
```

![image](https://github.com/user-attachments/assets/7c146e15-9c12-48f9-83a9-3b6c37b93a83)


### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
```


![image](https://github.com/user-attachments/assets/de15de86-3bf0-480b-916e-88f8e5395c5e)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
