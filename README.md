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
# DEVELOPED BY: S.Harika
# REGISTER NO: 212224240155

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
cv2.putText(img, 'HARIKA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
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
<img width="635" height="132" alt="Screenshot 2025-10-08 232108" src="https://github.com/user-attachments/assets/7e99a5c5-bca0-4cbb-8044-cbb5af9a5e9b" />

### Display the result of Opening
<img width="638" height="125" alt="Screenshot 2025-10-08 232332" src="https://github.com/user-attachments/assets/09c440b2-0e46-4419-be1e-e82b97205521" />

### Display the result of Closing
<img width="619" height="116" alt="Screenshot 2025-10-08 232405" src="https://github.com/user-attachments/assets/58e0b454-8fcc-420e-a3db-9427a9650a81" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
