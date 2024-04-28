# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'VENKATA RATHNAM',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image

![image](https://github.com/pochireddyp/erosion--dilation/assets/150232043/a4674fa9-0193-4f56-ba0c-6db5da866aa1)

### Display the Eroded Image
![image](https://github.com/pochireddyp/erosion--dilation/assets/150232043/c5b7b9a9-f4da-4c92-a1ee-0e86ea352b5f)


### Display the Dilated Image
![image](https://github.com/pochireddyp/erosion--dilation/assets/150232043/4e28d4f4-434c-4f84-9bd2-1c2aa5e23d4d)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
