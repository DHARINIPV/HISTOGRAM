# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```
# Developed By: Dharini PV
# Register Number: 212222240024
```
# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('RE.jpg')
color_image = cv2.imread('bugatti.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("RE.jpg")
color_image = cv2.imread("bugatti.jpg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
```
# Write the code to perform histogram equalization of the image. 
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('BMW.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot from 2023-09-05 09-22-37](https://github.com/DHARINIPV/HISTOGRAM/assets/119400845/94e36438-5c1f-4e93-8365-af516ea9b450)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot from 2023-09-05 09-24-37](https://github.com/DHARINIPV/HISTOGRAM/assets/119400845/50ab4f5b-b5d4-40a3-92df-c75cd9bed411)
![Screenshot from 2023-09-05 09-24-52](https://github.com/DHARINIPV/HISTOGRAM/assets/119400845/8ef63b84-a609-4fca-936e-004f08c727e8)

### Histogram Equalization of Grayscale Image
![Screenshot from 2023-09-05 09-36-15](https://github.com/DHARINIPV/HISTOGRAM/assets/119400845/90650b11-aafe-487f-be66-377273f3d185)
![Screenshot from 2023-09-05 09-35-09](https://github.com/DHARINIPV/HISTOGRAM/assets/119400845/cec90f84-5518-4fd9-871b-45d0222e4ff7)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
