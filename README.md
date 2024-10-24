#  Ex 10 - OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1: 
Import the required libraries.
### Step 2: 
Create a text image using cv2.putText().
### Step 3: 
Define a structuring element (kernel) for the morphological operations.
### Step 4: 
Apply the Opening operation using cv2.morphologyEx() with the cv2.MORPH_OPEN flag.
### Step 5: 
Apply the Closing operation using cv2.morphologyEx() with the cv2.MORPH_CLOSE flag.
 
## Program:
### Developed by : kathiravan
### Reg.no :212222230063
```
# Import the necessary packages
import cv2
import numpy as np
image = np.zeros((300, 700), dtype="uint8")

# Create the Text using cv2.putText
cv2.putText(image, 'Opening & Closing', (30, 150), cv2.FONT_HERSHEY_SIMPLEX, 2, (255, 255, 255), 5)

# Create the structuring element
kernel = np.ones((5, 5), np.uint8)

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

### Display the input Image
![Screenshot 2024-10-23 093300](https://github.com/user-attachments/assets/730461d3-94a2-404c-ab56-9e1c15136110)


### Display the result of Opening
![Screenshot 2024-10-23 093310](https://github.com/user-attachments/assets/6c7f4cb2-6171-4e88-8933-1c5de44a80f1)


### Display the result of Closing
![Screenshot 2024-10-23 093320](https://github.com/user-attachments/assets/0de87acf-e71a-4b23-836e-0dfc4265635e)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
