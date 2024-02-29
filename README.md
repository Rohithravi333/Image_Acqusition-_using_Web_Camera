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
<br>Import OpenCV Package.

### Step 2:
<br>Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
<br>Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
<br>Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
<br>Display Video or Image. Use 'imshow' to display the captured video frame or image, and end Program with 'q'. Allow the program to be terminated by pressing the 'q' key.

## Program:
Python
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
    cv2.imshow('212222230121_rohith',image)
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
    cv2.imshow('212222230121_rohith',image)
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

![Screenshot 2024-02-29 140235](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/2b74b40a-e431-465c-9c6a-c7c4ec58dd25)




### iv) Rotate and display the video
</br>
</br>
![Screenshot 2024-02-29 140252](https://github.com/Rohithravi333/Image_Acqusition-_using_Web_Camera/assets/119394126/467776c6-cd3e-4953-a23c-21769d4f80b8)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
