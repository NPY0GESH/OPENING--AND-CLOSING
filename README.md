# OPENING--AND-CLOSING

NAME: N P YOGESH


REGISTER NO: 212225240189
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

img = np.zeros((300, 600), dtype='uint8')

font = cv2.FONT_ITALIC

cv2.putText(img, "Venkat", (5, 150), font, 3, 255, 5, cv2.LINE_AA)

kernel_open = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
kernel_close = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))

opened = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel_open)

closed = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel_close)

plt.figure(figsize=(15, 5))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap='gray')
plt.title("Original")
plt.axis('off')

plt.subplot(1, 3, 2)
plt.imshow(opened, cmap='gray')
plt.title("Opening")
plt.axis('off')

plt.subplot(1, 3, 3)
plt.imshow(closed, cmap='gray')
plt.title("Closing")
plt.axis('off')

plt.show()
```
## Output:

### Display the input Image
<br>
<br>
<br>
<img width="194" height="102" alt="image" src="https://github.com/user-attachments/assets/11536c72-923f-4baa-a2e8-d15b742539df" />


<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>
<img width="195" height="98" alt="image" src="https://github.com/user-attachments/assets/3c87c438-66d2-44ae-a94e-72b48d07abff" />


<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>
<img width="166" height="84" alt="image" src="https://github.com/user-attachments/assets/8dff66e7-450d-4592-8821-536e48a9e258" />


<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
