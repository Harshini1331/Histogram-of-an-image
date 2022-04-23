# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
### Developed By: Harshini M
### Register Number: 212220230022
```python
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

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
<br>
<img width="216" alt="image" src="https://user-images.githubusercontent.com/75235554/164910014-c3645e59-fbd5-4ae8-8450-a9c3a973b9d5.png">
<br>
<img width="322" alt="image" src="https://user-images.githubusercontent.com/75235554/164910026-ff74da6a-ab6d-45ee-b298-85135e299d09.png">
<br>

### Histogram of Grayscale Image and any channel of Color Image
<br>
<img width="423" alt="image" src="https://user-images.githubusercontent.com/75235554/164910060-4b96e36e-f75a-4cc8-9696-e4826dc6525c.png">
<br>
<img width="392" alt="image" src="https://user-images.githubusercontent.com/75235554/164910072-fff3047c-c814-4f61-a848-4c74c60f79cf.png">
<br>

### Histogram Equalization of Grayscale Image
<br>
<img width="357" alt="image" src="https://user-images.githubusercontent.com/75235554/164910123-5c51bfa3-fab9-45a3-8317-11d346cc9a2e.png">
<br>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
