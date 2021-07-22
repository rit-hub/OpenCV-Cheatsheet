
## Play Video & Acess Camera using OpenCV

Play single video

```bash
  import numpy as np
  import cv2

  video_path1 = r'D:\**********.mp4'
  video_path2 = r'D:\*********.mp4'

  cap = cv2.VideoCapture(video_path1)
  while cap.isOpened():
    ret, frame = cap.read()
    if ret:
      image = cv2.resize(frame, (600, 400))
      cv2.imshow(image)
      if cv2.waitKey(25) & 0xff == ord('q'):
        break
    else:
      break
  
  cap.release()
  cv2.destroyAllWindows()
```
Access Camera

```bash
  import numpy as np
  import cv2

  cap = cv2.VideoCapture(0)   #Primary camera
  #cap = cv2.VideoCapture(1)  #secoendary camera
  #cap = cv2.VideoCapture(-1) #secoendary camera
  #cap = cv2.VideoCapture(***camera name**)

  while cap.isOpened():
    ret, frame = cap.read()
    if ret:
      image = cv2.resize(frame, (600, 400))
      cv2.imshow(image)
      if cv2.waitKey(25) & 0xff == ord('q'):
        break
    else:
      break
  
  cap.release()
  cv2.destroyAllWindows()
```


