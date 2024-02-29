# Image_Acqusition-_using_Web_Camera
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>

### Step 2:
<br>

### Step 3:
<br>

### Step 4:
<br>

### Step 5:
<br>

## Program:
``` Python
### Developed By:roith r
### Register No:212222230121

## i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Fer.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```

## ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('Car',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230027_dario',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video


```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230027_dario',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```




```
## Output

### i) Write the frame as JPG image
</br>![Screenshot 2024-02-29 134129](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/49533f73-50ee-47b2-ae9e-12cdd2e92253)

</br>


### ii) Display the video
</br>

</br>![Screenshot 2024-02-29 134621](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/6aca496a-8f86-4749-9e7e-cef55be304d4)



### iii) Display the video by resizing the window
</br>
</br>


![Screenshot 2024-02-29 135103](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/9dbf4773-52d0-4bda-a885-526ded8d714c)


### iv) Rotate and display the video
</br>
</br>![Screenshot 2024-02-29 135314](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/c7a44c32-8bae-4643-8693-bab190e76101)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
