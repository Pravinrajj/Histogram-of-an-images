# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:

```python
Developed By: PRAVINRAJJ G.K
Register Number: 212222240080
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("tree.jpg")
color_image = cv2.imread("tree1.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("tree.jpg")
Color_image = cv2.imread("tree1.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("tree.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
<img height=45% width=45% src="https://github.com/Pravinrajj/Histogram-of-an-images/assets/117917674/9b69e47a-1c02-4116-a5ce-b96778b0c5fa">
<img height=47% width=45% src="https://github.com/Pravinrajj/Histogram-of-an-images/assets/117917674/6993ab5e-e97f-4270-8a94-cdaf3aed4239">

### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -
![2](https://github.com/Gokul-008/Histogram-of-an-images/assets/121165996/ebb0d5d4-c87f-4972-8e3a-10337b3bf4cd)
![3](https://github.com/Gokul-008/Histogram-of-an-images/assets/121165996/8e2de08a-8d8b-456c-a572-e107de945c62)

#### Green Channel -
![4](https://github.com/Gokul-008/Histogram-of-an-images/assets/121165996/c4190837-f00c-4305-935a-8a9f22de6ec3)
![5](https://github.com/Gokul-008/Histogram-of-an-images/assets/121165996/6db58237-1094-4ca8-b6d9-ead7aa2e8f2e)

### Histogram Equalization of Grayscale Image :
![6](https://github.com/Gokul-008/Histogram-of-an-images/assets/121165996/d853f50c-0fce-4c98-a76d-50e3e516f456)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
