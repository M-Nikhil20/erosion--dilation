# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image = np.zeros((300, 600, 3), dtype="uint8")
text = "OpenCV Demo"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
plt.show()

# Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
plt.show()

```
## Output:

### Display the input Image

![image](https://github.com/user-attachments/assets/0c45e5d8-796f-4d15-8cdc-0b6622517c73)

### Display the Eroded Image

![image](https://github.com/user-attachments/assets/8285d2d4-a4f5-409e-a74f-6a46d6c303b2)

### Display the Dilated Image

![image](https://github.com/user-attachments/assets/c97b3cd5-5de1-4e92-bd40-3a54bac2f305)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
