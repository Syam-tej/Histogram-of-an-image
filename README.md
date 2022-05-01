# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import all the necessary libraries.

## Step2:
Read the images using imread() function.

## Step3:
Using calcHist() we can find the histogram of the images.

## Step4:
Using equalizeHist() we can equalize the image.

## Step5:
Using matplotlib.pyplot plot the histogram.
## Program:
```python
# Developed By:P.SYAM TEJ
# Register Number:212221240056
import cv2
import matplotlib.pyplot as plt

## Write your code to find the histogram of gray scale image and color image channels.
gray_image = cv2.imread("butterfly.jpg")
plt.imshow(gray_image)
plt.show()
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Grayscale value')
plt.ylabel('Pixel Count')
plt.stem(hist)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image
color_image=cv2.imread("venice.jpg")
plt.imshow(color_image)
plt.show()
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(hist1)
plt.show()




# Write the code to perform histogram equalization of the image. 
gray_image = cv2.imread('butterfly.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()






```
## Output:
### Input Grayscale Image and Color Image
![1](https://user-images.githubusercontent.com/93427224/166134644-4b11c597-c051-4d79-9fdc-288da87a0081.png)


### Histogram of Grayscale Image and any channel of Color Image
![2](https://user-images.githubusercontent.com/93427224/166134650-b4b96aa8-4fc5-43cc-b3bb-628a5eba9152.png)


### Histogram Equalization of Grayscale Image
![3](https://user-images.githubusercontent.com/93427224/166134653-1e55bcad-6cdf-4e74-ae75-39828ecdb069.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
