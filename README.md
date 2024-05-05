# EXP.9 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate  the image

 
## Program:

###  Import the necessary packages
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```py
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"SERENDIPITY",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```
###  Create the structuring element
```py
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
### Erode the image
```py
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
### Dilate the image
```py
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![Screenshot 2024-05-05 171457](https://github.com/KameshLeVI/erosion--dilation/assets/120780633/78e03d03-3dab-4a62-bcbf-f52ffe56801a)


### Display the Eroded Image
![Screenshot 2024-05-05 171504](https://github.com/KameshLeVI/erosion--dilation/assets/120780633/2f9a7ca4-8143-4648-b9b4-06257270583d)



### Display the Dilated Image
![Screenshot 2024-05-05 171517](https://github.com/KameshLeVI/erosion--dilation/assets/120780633/4a6870c7-7004-47bb-af23-0271349fa945)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
