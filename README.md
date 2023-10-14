# EX-11 OPENING CLOSING OPERATIONS
### Aim:
To implement Opening and Closing using Python and OpenCV.
### Software Required
Anaconda - Python 3.7 , OpenCV.
### Algorithm:
- Step1: Import the necessary packages.
- Step2: Read the image.
- Step3: Create the structuring element or kernal element.
- Step4: Use Opening operation.
- Step5: Use Closing Operation.
```
Developed By: ROHIT JAIN D
Register No: 212222230120
```
### Program:
- Importing the necessary packages.
  ```Python
  import cv2
  import numpy as np
  ```
- Create the Text using cv2.putText.
  ```Python
  img=np.zeros((100,500),dtype='uint8')
  font=cv2.FONT_HERSHEY_PLAIN
  cv2.putText(img,'ROHIT JAIN D 212222230120',(5,60),font,2,(255),5,cv2.LINE_AA)
  cv2.imshow("Original Image",img)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-11-OPENING-CLOSING-OPERATIONS/assets/118707073/f4ea3d7d-f985-42ef-aa17-0014c582eed2">

- Create the structuring element.
  ```Python
  kernal=np.ones((5,5),np.uint8)
  ```
- Use Opening operation.
  ```Python
  imgO=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernal)
  cv2.imshow("Opening Operation",imgO)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-11-OPENING-CLOSING-OPERATIONS/assets/118707073/5e2ede03-4a08-49e2-8c35-70b199094962">

- Use Closing Operation.
  ```Python
  imgC=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernal)
  cv2.imshow("Closing Operation",imgC)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-11-OPENING-CLOSING-OPERATIONS/assets/118707073/298b2514-9ba7-4e94-9873-b8be10a67194">

### Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
