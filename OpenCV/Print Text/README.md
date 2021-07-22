
## Print text on an image

Write Text on Image

```bash
  import cv2
import numpy as np
 
img_path = r"C:\Users\k.jpg"
 
image = cv2.imread(img_path)
image = cv2.resize(image, (1280, 720))
 
text = "Model"
org = (100, 200)
font = cv2.FONT_HERSHEY_COMPLEX
fontScale = 6
color = (0,0,255)  #(B, G, R)
thickness = 3
lineType = cv2.LINE_AA
bottomLeftOrigin = False
 
# Syntax>> cv2.putText(image, text, org, font, fontScale,
 color[, thickness[, lineType[, bottomLeftOrigin]]])
 
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin)
 
cv2.imshow("Text Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Print text Inverse

```bash
  import cv2
import numpy as np
 
img_path = r"C:\Users\k.jpg"
 
image = cv2.imread(img_path)
 
image = cv2.resize(image, (1280, 720))
 
text = "Model"
org = (100, 200)
font = cv2.FONT_HERSHEY_COMPLEX
fontScale = 6
 
color = (0,0,255)  #(B, G, R)
thickness = 3
lineType = cv2.LINE_AA
bottomLeftOrigin = True
 
# cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]])
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin)
 
 
cv2.imshow("Text Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```

Print text with reflection

```bash
  import cv2
import numpy as np
 
img_path = r"C:\Users\k.jpg"
 
image = cv2.imread(img_path)
 
image = cv2.resize(image, (1280, 720))
 
text = "Model"
org = (100, 200)
font = cv2.FONT_HERSHEY_COMPLEX
fontScale = 6
 
color = (0,0,255)  #(B, G, R)
thickness = 3
lineType = cv2.LINE_AA
bottomLeftOrigin = True
 
# cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]])
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin)
 
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin=False)
 
cv2.imshow("Text Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```

Text with different color and font with size

```bash
  import cv2
import numpy as np
 
img_path = r"C:\Users\k.jpg"
 
image = cv2.imread(img_path)
 
image = cv2.resize(image, (1280, 720))
 
text = "Indian AI Production"
org = (50, 100)
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
fontScale = 4
 
color = (87,67,23)  #(B, G, R)
thickness = 3
lineType = cv2.LINE_AA
bottomLeftOrigin = True
 
# cv2.putText(image, text, org, font, fontScale, color[, thickness[, lineType[, bottomLeftOrigin]]])
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin)
 
img_text = cv2.putText(image, text, org, font, fontScale, color, thickness, lineType, bottomLeftOrigin=False)
 
cv2.imshow("Text Image", img_text)
 
cv2.waitKey(0)
cv2.destroyAllWindows()
```

Font Style

```bash
 //! Only a subset of Hershey fonts
enum HersheyFonts {
    FONT_HERSHEY_SIMPLEX        = 0, //!< normal size sans-serif font
    FONT_HERSHEY_PLAIN          = 1, //!< small size sans-serif font
    FONT_HERSHEY_DUPLEX         = 2, //!< normal size sans-serif font (more complex than FONT_HERSHEY_SIMPLEX)
    FONT_HERSHEY_COMPLEX        = 3, //!< normal size serif font
    FONT_HERSHEY_TRIPLEX        = 4, //!< normal size serif font (more complex than FONT_HERSHEY_COMPLEX)
    FONT_HERSHEY_COMPLEX_SMALL  = 5, //!< smaller version of FONT_HERSHEY_COMPLEX
    FONT_HERSHEY_SCRIPT_SIMPLEX = 6, //!< hand-writing style font
    FONT_HERSHEY_SCRIPT_COMPLEX = 7, //!< more complex variant of FONT_HERSHEY_SCRIPT_SIMPLEX
    FONT_ITALIC                 = 16 //!< flag for italic font
};
```
LineTyle

```bash
 cv::LineTypes {
  cv::FILLED = -1,
  cv::LINE_4 = 4,
  cv::LINE_8 = 8,
  cv::LINE_AA = 16
```