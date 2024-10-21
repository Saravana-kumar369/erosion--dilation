# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1: Import necessary libraries such as OpenCV and Numpy.
### Step 2: Create a text image using cv2.putText().
### Step 3: Create the structuring element using cv2.getStructuringElement().
### Step 4: Perform erosion on the image using cv2.erode().
### Step 5: Perform dilation on the image using cv2.dilate().
## Program:

``` Python
# Import the necessary library
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the text image using cv2.putText
img1 = np.zeros((100, 400), dtype='uint8')  
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1, 'TheAILearner', (5, 70), font, 2, (255), 5, cv2.LINE_AA)

# Display the input image
plt.imshow(img1, cmap='gray')
plt.title("Input Image")
plt.show()

# Create the structuring element
kernel = np.ones((5, 5), np.uint8) 
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS, (7, 7))  

# Erode the image
image_erode = cv2.erode(img1, kernel1)

# Display the eroded image
plt.imshow(image_erode, cmap='gray')
plt.title("Eroded Image")
plt.show()

# Dilate the image
image_dilate = cv2.dilate(img1, kernel1)

# Display the dilated image
plt.imshow(image_dilate, cmap='gray')
plt.title("Dilated Image")
plt.show()

```
## Output:

### Display the input Image
<br>

![image](https://github.com/user-attachments/assets/6d4dc736-0c4c-4c5d-8f95-3276fcbc0f21)

<br>

### Display the Eroded Image
<br>

![image](https://github.com/user-attachments/assets/0ab4b18d-8bd1-4b42-ac1c-42e9e8c0abeb)

<br>

### Display the Dilated Image
<br>

![image](https://github.com/user-attachments/assets/7b32d13d-f591-413d-b826-ea37bad13730)

<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
