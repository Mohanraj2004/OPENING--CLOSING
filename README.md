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
Developed By: Mohan Raj
Register No: 212221230065
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
  cv2.putText(img,'Mohan Raj',(5,60),font,2,(255),5,cv2.LINE_AA)
  cv2.imshow("Original Image",img)
  cv2.waitKey(0)
  ```
![Screenshot 2023-10-14 225841](https://github.com/Mohanraj2004/OPENING--CLOSING/assets/132890483/0962e171-5fd4-44b8-957e-9f6f7269cfa7)

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
![Screenshot 2023-10-14 225936](https://github.com/Mohanraj2004/OPENING--CLOSING/assets/132890483/9ae82e46-96ba-45b2-86cc-d6b6d9737a32)

- Use Closing Operation.
  ```Python
  imgC=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernal)
  cv2.imshow("Closing Operation",imgC)
  cv2.waitKey(0)
  ```
![Screenshot 2023-10-14 230020](https://github.com/Mohanraj2004/OPENING--CLOSING/assets/132890483/d351b537-11c4-4cf4-b36a-6bd85701ad56)

### Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
