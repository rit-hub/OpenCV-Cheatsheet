
## Cv2.Imshow() Function In Detail

OpenCV library has powerful function named as cv2.imshow(). Which shows the NumPy array in the form of an Image.

cv2.imshow() function takes any size of NumPy array and shows the image in the same size in the window. If the image resolution is more than a system screen resolution then it shows only those pixel which fits in the screen.

Ex: Image resolution is (2000,1000) (widht, height) and screen resolution is (1000,500). Then cv2.imshow() function shows only (1000,500) pixels of image not all. To solve this problem you can resize your image then show using cv2.imsho() function.

Syntax: cv2.imshow( windows_name, numpy_array)
windows_name: string value
numpy_array: 2d or 3d NumPy array

Draw Rectangle on Image

```bash
import cv2
import numpy as np
 
matx = np.zeros((200,200)) # numpy array with width =200, height=200
 
cv2.imshow("Zeros matx", matx) # show numpy array
 
cv2.waitKey(0) # wait for ay key to exit window
cv2.destroyAllWindows() # close all windows
```
Show Image

```bash
 import cv2
 
img_path = "model.jpg" # image name
img = cv2.imread(img_path) #  read image and store in numpy array
 
cv2.imshow("Model image", img)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Show same image in multiple windows

```bash
 import cv2
 
img_path = "model.jpg" # image name
 
img = cv2.imread(img_path)
 
# Showing same image in 3 windows
cv2.imshow("Model image 1", img)
cv2.imshow("Model image 2 ", img)
cv2.imshow("Model image 3", img)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
