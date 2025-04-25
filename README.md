# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Translation moves the image along the x or y-axis.
<br>

### Step2:
Scaling resizes the image by scaling factors.
<br>

### Step3:
Shearing distorts the image along one axis.
<br>

### Step4:
Reflection flips the image horizontally or vertically.
<br>

### Step5:
Rotation rotates the image by a given angle.
<br>

## Program:

## NAME: DURGA V
## REG NO: 212223230052

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('dhdd.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')

_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')


plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')


plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

plt.tight_layout()
plt.show()




```
## Output

### Original Image

![image](https://github.com/user-attachments/assets/c7cca671-51fb-4ae5-ba98-67d99ef574d2)


### Global Thresholding

![image](https://github.com/user-attachments/assets/af55f7ae-4a6f-4241-baf2-00f9464fe2e3)


### Adaptive Thresholding

![image](https://github.com/user-attachments/assets/04a73d75-1944-47cc-ac24-bea04b6688a4)


### Optimum Global Thesholding using Otsu's Method


![image](https://github.com/user-attachments/assets/c267c901-cd76-45ae-b759-8e526e547e86)



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
