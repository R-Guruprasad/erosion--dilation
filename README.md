# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the required libraries.
### Step 2: 
Create a text image using cv2.putText().
### Step 3: 
Define a structuring element for the erosion and dilation operations.
### Step 4: 
Apply erosion to the image using cv2.erode().
### Step 5: 
Apply dilation to the image using cv2.dilate().
### Step 6: 
Display the original, eroded, and dilated images.
## Program:

``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the input image using cv2.imread()
image = cv2.imread("im.jpeg")  # Replace with the path to your image file

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Step 3: Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)

# Step 4: Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Convert images from BGR to RGB for Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

# Plot the original, eroded, and dilated images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()


```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/e362dec8-b151-46e1-8d78-5b936368cda6)

### Display the Eroded Image

![image](https://github.com/user-attachments/assets/9fed8f8f-4e96-4c0d-aa41-6599f37bb8fa)

### Display the Dilated Image

![image](https://github.com/user-attachments/assets/9f2d3cf9-2b60-445b-b3d5-b52c1014e377)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
