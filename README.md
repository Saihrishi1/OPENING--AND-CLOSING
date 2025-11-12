# OPENING--AND-CLOSING

### Name : Sai Hrishi M
### Reg No : 212224240140

## Aim

To implement Opening and Closing using Python and OpenCV.

## Software Required

1. Anaconda - Python 3.7
2. OpenCV
3. 
## Algorithm:

### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText.

### Step3:

Create the structuring element.

### Step4:

Use Opening operation.

### Step5:

Use Closing Operation.

## Program:

```py

import cv2
import numpy as np
import matplotlib.pyplot as plt
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Sai Hrishi M', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)

plt.axis("off")
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")


```
## Output:

### Display the input Image

<img width="528" height="143" alt="image" src="https://github.com/user-attachments/assets/ef43295e-a248-40ea-b3be-9cdd8aa4a13d" />


### Display the result of Opening

<img width="528" height="143" alt="image" src="https://github.com/user-attachments/assets/803023ec-3258-4fe8-9684-aa8d30a04da7" />


### Display the result of Closing

<img width="509" height="146" alt="image" src="https://github.com/user-attachments/assets/648e7935-ced3-4e12-bcbb-34dbf5107428" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
