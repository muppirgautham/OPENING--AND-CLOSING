# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step1: Import the necessary packages

Step2: Give the input text using cv2.putText()

Step3: Perform opening operation and display the result

Step4: Similarly, perform closing operation and display the result

 
## Program:
```
Name: M gautham
Register No: 212221230027
```

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img1,'AEROSPACE',(4,70), font,1,(255),5,cv2.LINE_AA)
```

# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

# Use Opening operation
```
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```

# Use Closing Operation
```
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```


## Output:

### Display the input Image
![image](https://github.com/muppirgautham/OPENING--AND-CLOSING/assets/94810884/1d34c20f-c0e2-4646-83d7-39fe37e0e7b8)

### Display the result of Opening
![image](https://github.com/muppirgautham/OPENING--AND-CLOSING/assets/94810884/42568dad-818d-4ebd-aa21-dcc196f7586e)


### Display the result of Closing
![image](https://github.com/muppirgautham/OPENING--AND-CLOSING/assets/94810884/2364e216-c651-4781-b987-ee2043a21aa3)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
