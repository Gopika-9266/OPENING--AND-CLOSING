# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the required libraries.


### Step2:
Create a text image using cv2.putText().

### Step3:
Define a structuring element (kernel) for the morphological operations.

### Step4:
Apply the Opening operation using cv2.morphologyEx() with the cv2.MORPH_OPEN flag.

### Step5:
pply the Closing operation using cv2.morphologyEx() with the cv2.MORPH_CLOSE flag.

 
## Program:

```
Name: Gopika R
Reg No: 212222240031
```
```
# Import the necessary packages
import cv2
import numpy as np
image = np.zeros((300, 500), dtype="uint8")

# Create the Text using cv2.putText
cv2.putText(image, 'Gopika', (130, 150), cv2.FONT_HERSHEY_SIMPLEX, 2, (255, 255, 255), 5)

# Create the structuring element
kernel = np.ones((4, 5), np.uint8)

# Use Opening operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

cv2.imshow('Input Image', image)
cv2.imshow('Opened Image', opened_image)
cv2.imshow('Closed Image', closed_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Display the input Image :
![Screenshot 2024-11-10 183909](https://github.com/user-attachments/assets/e25e5624-089e-4441-ab53-0c954c1b447e)

### Display the result of Opening :

![Screenshot 2024-11-10 183859](https://github.com/user-attachments/assets/28387f9d-81f4-43c0-85b4-7ceffd66d95b)

### Display the result of Closing :
![Screenshot 2024-11-10 183845](https://github.com/user-attachments/assets/d7f11b3d-b278-443e-b4d0-4bdb80c6092c)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
