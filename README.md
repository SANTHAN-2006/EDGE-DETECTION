# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program :
```python
# Reg No : 212223240065
# Name : K. SANTHAN KUMAR
import cv2
# Read the image
image = cv2.imread('dog.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Gaussian blur
img_blurred = cv2.GaussianBlur(gray_image, (3, 3), 0)

# Sobel edge detection
sobelx = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 0, ksize=5)
sobely = cv2.Sobel(img_blurred, cv2.CV_64F, 0, 1, ksize=5)
sobelxy = cv2.Sobel(img_blurred, cv2.CV_64F, 1, 1, ksize=5)

# Laplacian edge detection
laplacian = cv2.Laplacian(img_blurred, cv2.CV_64F)

# Canny edge detection
canny_edges = cv2.Canny(img_blurred, 120, 150)

# Display images
cv2.imshow('Original', gray_image)
cv2.imshow('Sobel X', sobelx)
cv2.imshow('Sobel Y', sobely)
cv2.imshow('Sobel XY', sobelxy)
cv2.imshow('Laplacian', laplacian)
cv2.imshow('Canny Edges', canny_edges)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### SOBEL EDGE DETECTOR

![image](https://github.com/SANTHAN-2006/EDGE-DETECTION/assets/80164014/fe67270e-8c0f-4dc6-b8ff-32bce6c191de)


### LAPLACIAN EDGE DETECTOR
![image](https://github.com/SANTHAN-2006/EDGE-DETECTION/assets/80164014/722ca6e0-23dc-438c-83a0-c3a53d233511)


### CANNY EDGE DETECTOR
![image](https://github.com/SANTHAN-2006/EDGE-DETECTION/assets/80164014/c6257d21-c29c-4732-9590-670a9718f37e)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
