# OPENING--AND-CLOSING

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
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
### Import the necessary packages
```
import cv2
import numpy as np
```

### Create the Text using cv2.putText
```
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Telecast', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```

### Create the structuring element
```
struct_ele = np.ones((9, 9), np.uint8)
```

### Use Opening operation
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```

### Use Closing Operation
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```

## Output:
### Display the input Image
<img width="603" alt="326270180-6d4777fb-c35e-423c-87c3-6695640dddc5" src="https://github.com/Priya-Loganathan/OPENING--AND-CLOSING/assets/121166075/7a834a5e-03a5-43ab-a329-96c4ea52bcff">

### Display the result of Opening
<img width="571" alt="326270345-de9b815c-5789-47f6-97dc-32610b49fe2e" src="https://github.com/Priya-Loganathan/OPENING--AND-CLOSING/assets/121166075/73cb39ce-2961-4846-a639-04b48f81925b">

### Display the result of Closing
<img width="532" alt="326270379-26d909f1-d571-41d1-8977-28ccf399dd85" src="https://github.com/Priya-Loganathan/OPENING--AND-CLOSING/assets/121166075/46b77707-2dba-439b-a107-7f407befcdf2">

## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
