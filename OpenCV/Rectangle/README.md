
## Draw Rectangle, Print Text On An Image

Draw Rectangle on Image

```bash
import cv2
import numpy as np
 
img_path = r"C:\Users.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
pt1 = (400, 40)
pt2 = (800, 300)
color = (0, 255, 0)
thickness = 4
lineType = cv2.LINE_4
 
#rectangle(img, pt1, pt2, color[, thickness[, lineType[, shift]]])
img_rect = cv2.rectangle(image, pt1, pt2, color, thickness, lineType)
 
cv2.imshow("Rectangle on Image", img_rect)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Fill Rectangle on Image

```bash
 import cv2
import numpy as np
 
img_path = r"C:\Users\k567.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
pt1 = (400, 40)
#pt1 = (800, 40)
pt2 = (800, 300)
color = (255, 0, 0)
thickness = -1
lineType = cv2.LINE_4
 
#rectangle(img, pt1, pt2, color[, thickness[, lineType[, shift]]])
img_rect = cv2.rectangle(image, pt1, pt2, color, thickness, lineType)
 
cv2.imshow("Rectangle on Image", img_rect)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Text On Rectangle on Image

```bash
 import cv2
import numpy as np
 
img_path = r"C:\Users\67.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
pt1 = (400, 40)
pt2 = (800, 300)
color = (255, 0, 0)
thickness = -1
lineType = cv2.LINE_4
 
#rectangle(img, pt1, pt2, color[, thickness[, lineType[, shift]]])
img_rect = cv2.rectangle(image, pt1, pt2, color, thickness, lineType)
 
#text on image
text = "Face - 100%"
org = (500, 170)
fontFace = cv2.FONT_HERSHEY_SIMPLEX
fontScale = 1
color = (0,255,25)
lineType = cv2.LINE_4
 
#text, org, fontFace, fontScale, color[, thickness
 
img_text = cv2.putText(img_rect, text, org, fontFace, fontScale, color, lineType)
 
 
cv2.imshow("Rectangle on Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```

Text Above Rectangle on Image

```bash
import cv2
import numpy as np
 
img_path = r"C:\Users842567.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
pt1 = (400, 40)
pt2 = (800, 300)
color = (255, 0, 0)
thickness = 4
lineType = cv2.LINE_4
 
#rectangle(img, pt1, pt2, color[, thickness[, lineType[, shift]]])
img_rect = cv2.rectangle(image, pt1, pt2, color, thickness, lineType)
 
#text on image
text = "Face - 100%"
org = (400, 30)
fontFace = cv2.FONT_HERSHEY_SIMPLEX
fontScale = 1
color = (0,255,25)
lineType = cv2.LINE_4
 
#text, org, fontFace, fontScale, color[, thickness
 
img_text = cv2.putText(img_rect, text, org, fontFace, fontScale, color, lineType)
 
 
cv2.imshow("Rectangle on Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```

Save image

```bash
 import cv2
import numpy as np
 
img_path = r"C:\User42567.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
pt1 = (400, 40)
pt2 = (800, 300)
color = (255, 0, 0)
thickness = 4
lineType = cv2.LINE_4
 
#rectangle(img, pt1, pt2, color[, thickness[, lineType[, shift]]])
img_rect = cv2.rectangle(image, pt1, pt2, color, thickness, lineType)
 
#text on image
text = "Face - 100%"
org = (400, 30)
fontFace = cv2.FONT_HERSHEY_SIMPLEX
fontScale = 1
color = (0,255,25)
lineType = cv2.LINE_4
 
#text, org, fontFace, fontScale, color[, thickness
 
img_text = cv2.putText(img_rect, text, org, fontFace, fontScale, color, lineType)
 
 
cv2.imwrite("image_with_rect_text.png", img_text)
 
cv2.imshow("Rectangle on Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
