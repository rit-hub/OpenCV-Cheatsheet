
## Read & Show Images in OpenCV

Read & show image
```bash
  import cv2
  path = r"c:\{directory path}"
  img_name = "image-name.jpg"

  img = cv2.imread(path + '\\' + img_name)

  cv2.imshow('Window_name_xyz', img)
  cv2.waitKey(0)

  cv2.destroyAllWindows()
```
show resized image in ovenCV

```bash
  import cv2
  path = r"c:\{directory path}"
  img_name = "image-name.jpg"

  img = cv2.imread(path + '\\' + img_name)

  cv2.resize(img, (600, 400))

  cv2.imshow('Window_name_xyz', img)
  cv2.waitKey(0)

  cv2.destroyAllWindows()
```
Slide show image in ovenCV

```bash
  import cv2
  import os
  img_names = os.listdir('data\images')
  img_names

  path = r"c:\{directory path}"
  
  for img_name in img_names:
    img = cv2.imread(path + img_name)
    cv2.resize(img, (600, 400))
    cv2.imshow('Window_name_xyz', img)

    cv2.waitKey(0.5)
    #cv2.waitKey(1)
    #cv2.waitKey(0)

  cv2.destroyAllWindows()
```
Multiple images in one window

```bash
  import cv2
  import os
  import numpy as np

  img_names = os.listdir('data\images')
  path = r"c:\{directory path}"
  
  for img_name in img_names:
    img = cv2.imread(path + img_name)
    cv2.resize(img, (300, 200))
    img_2 = np.hstack((img, img))
    img_4 = np.vstack((img_2, img_2))
    cv2.imshow('Window_name_4 images', img_4)

    cv2.waitKey(1)
  cv2.destroyAllWindows()
```

6/9 images in one window

```bash
  import cv2
  import os
  import numpy as np

  img_names = os.listdir('data\images')
  path = r"c:\{directory path}"
  
  for img_name in img_names:
    img = cv2.imread(path + img_name)
    cv2.resize(img, (300, 200))
    img_3 = np.hstack((img, img, img))
    img_6 = np.vstack((img_3, img_3))
    #img_9 = np.vstack((img_3, img_3, img_3))
    cv2.imshow('Window_name_6 images', img_6)

    cv2.waitKey(1)

  cv2.destroyAllWindows()
```