# Implementation of Erosion and Dilation
## Aim:
To implement Erosion and Dilation using Python and OpenCV.
## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the text image using cv2.putText.

### Step3:

Then create the structuring image for dilation/erosion.

### Step4:

Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:

Plot the images using plt.imshow.
 
## Program:

### Developed by : KAYALVIZHI M
### Register Number: 212220230024

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Kayal",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```
## Output:

### Display the input Image

![img](https://user-images.githubusercontent.com/75413726/170735221-111442a3-2af2-4f24-86c9-49770e35397e.jpg)

### Display the Eroded Image

![img1](https://user-images.githubusercontent.com/75413726/170735344-d825d83a-b379-4f32-8196-5fc63b49a20e.jpg)

### Display the Dilated Image

![img2](https://user-images.githubusercontent.com/75413726/170735470-830d0168-5c88-4910-a0a4-89c988465a3c.jpg)

## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
