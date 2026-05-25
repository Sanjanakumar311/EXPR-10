# EX-10

# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
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
### DEVELOPED BY: SANJANA K L
### REGISTER NO: 212224230241

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JANARTHANAN K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image

<img width="351" height="372" alt="image" src="https://github.com/user-attachments/assets/f2fa7f3a-ca96-4b85-957e-bd309eb3142d" />





### Display the result of Opening
<img width="357" height="382" alt="image" src="https://github.com/user-attachments/assets/c60cd7f1-c964-4740-8c01-758b5a30be35" />




### Display the result of Closing
<img width="349" height="373" alt="image" src="https://github.com/user-attachments/assets/1f7bf86b-c3a9-4dae-a30d-99e9ffd2483c" />




## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
