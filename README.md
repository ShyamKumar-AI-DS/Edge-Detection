# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:

Import the required packages for further process.

### Step 2:

Read the image and convert the bgr image to gray scale image.

### Step 3:

Use any filters for smoothing the image to reduse the noise.

### Step 4:

Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step 5:

Display the filtered image using plot and imshow.
 
## Program:

```python 

# Import the packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("alaskan.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

```

```python

# SOBEL EDGE DETECTOR:

# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("animal.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("animal.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("animal.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python

# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("animal.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

```

```python 

# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("animal.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()

```
## Output:
###INPUT IMAGE
![Screenshot_20230419_103724](https://user-images.githubusercontent.com/93427182/232974208-6c78418a-4118-4983-a990-152b76a2ff65.png)

### SOBEL EDGE DETECTOR
### SOBEL-X:
![Screenshot_20230419_104539](https://user-images.githubusercontent.com/93427182/232974236-96a3b4e7-8147-49fb-85ac-04524dce9800.png)

### SOBEL-Y:
![Screenshot_20230419_104558](https://user-images.githubusercontent.com/93427182/232974242-0e5136c9-650c-4843-aab1-d446dc8edefb.png)

### SOBEL-XY:
![Screenshot_20230419_104723](https://user-images.githubusercontent.com/93427182/232974248-eddd30c8-18f9-40b1-85b7-6a9082e6ca99.png)


### LAPLACIAN EDGE DETECTOR
![Screenshot_20230419_104734](https://user-images.githubusercontent.com/93427182/232974258-ac6c6359-d33a-4110-bc9c-2d9bad1995a7.png)



### CANNY EDGE DETECTOR
![Screenshot_20230419_104747](https://user-images.githubusercontent.com/93427182/232974274-8b73a80e-a6e4-4d6e-9edb-467809bde0b2.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
