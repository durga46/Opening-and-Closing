## EX.NO : 11
## Date : 03.05.2022
# <p align="center"> Opening and Closing</p>
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
### Step2:
Create the text image using cv2.putText.
### Step3:
Then create the structuring element for opening and closing.
### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.
### Step5:
Plot the images using plt.imshow.
## Program:
```python
Developed by : Durga Devi P
Registeration Number:212220230015
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Durga Devi",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Output:
### Display the input Image

![Screenshot_709](https://user-images.githubusercontent.com/75235704/171369780-00e87fca-8ba1-4081-9a1e-49d525534efa.png)

### Display the result of Opening
![Screenshot_710](https://user-images.githubusercontent.com/75235704/171369800-f311d746-376c-4fe4-b37b-0e89cbdaf506.png)

### Display the result of Closing

![Screenshot_711](https://user-images.githubusercontent.com/75235704/171369833-766adf45-a6f7-439d-b353-2663324130ad.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
