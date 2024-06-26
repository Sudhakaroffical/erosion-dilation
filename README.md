# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## DEVELOPED BY SUDHAKAR K
## REG NO: 212222240107
## Algorithm:
### Step1:<br>
Import the necessary pacakages

### Step2:<br>
Create the text using cv2.putText

### Step3:<br>
Create the structuring element

### Step4:<br>
Erode the image


### Step5: <br>
Dilate the Image

 
## Program:


#### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
#### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'OREO',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
#### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
#### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
#### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
![Screenshot 2024-04-17 084042](https://github.com/Sudhakaroffical/erosion-dilation/assets/118622513/0af9acff-253c-465c-9900-e4280749a852)

### Display the Eroded Image

![Screenshot 2024-04-17 084119](https://github.com/Sudhakaroffical/erosion-dilation/assets/118622513/ac97ebf5-83f1-44d8-913b-4ee6a72cf11a)


### Display the Dilated Image

![Screenshot 2024-04-17 084133](https://github.com/Sudhakaroffical/erosion-dilation/assets/118622513/7f0b9974-ded0-45fa-a8a1-bd84ee03ee49)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
