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
### Grayscale image and Color image

import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.jpeg")
color_image = cv2.imread("dip.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

### Histogram of Grayscale image

import cv2
Gray_image = cv2.imread("gray.jpeg")
Color_image = cv2.imread("dip.jpeg")
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

### Histogram of Color image
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

### Histogram equalization of Grayscale image

import cv2
gray_image = cv2.imread("dip.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/56e9e135-7f0c-49ae-bd73-713dba9dca21)

![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/14af90c2-abbe-4931-bcc6-d5bc7f865e30)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/0d545692-88c0-4437-bf71-dfde6e73206e)
![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/3a5f4da6-3469-4496-9b6f-f38805eb25cc)
![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/16cb27a8-54b2-4402-b81a-ee6b6e64b726)
![image](https://github.com/MANOKARTHICK09/Histogram-of-an-images/assets/121785458/fb5b4d70-48d0-4e27-bfcd-d6a9d45c377f)



### Histogram Equalization of Grayscale Image.



![Uploading image.png…]()



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
