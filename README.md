# EX-09:Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:

Create a black image of size 100x600 pixels.
### Step-2:

Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3:

Show the image containing the text without axis labels.
### Step-4:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

## Program:
```
Developed By: Pavithra
Reference Number :212223230146
``` 
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Adchayakiruthika',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
![1](https://github.com/user-attachments/assets/40638ec7-0e13-4379-866d-e41a6c0df6a1)

# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
![2](https://github.com/user-attachments/assets/eb6642b7-e970-444b-987a-fa2285c68985)

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
![3](https://github.com/user-attachments/assets/226e07fb-8515-40b1-a52b-84306d9650d7)

# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
![4](https://github.com/user-attachments/assets/2045632c-1bf5-4e30-9354-c8d586de9fa3)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
