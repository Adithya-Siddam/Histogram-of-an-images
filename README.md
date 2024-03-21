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
```
 Developed By: Adithya Chowdary S.
 Register Number: 212221230100.
```
```python
import cv2
import matplotlib.pyplot as plt


gray_image=cv2.imread('leo.jpeg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

```
```python
color_image=cv2.imread('car1.jpeg')
hist1=cv2.calcHist([color_image],[1],None,[250],[0,250])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram of color image :Green channel")
plt.xlabel('intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
```python


gray_image = cv2.imread('leo.jpeg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![output01](https://github.com/Adithya-Siddam/Histogram-of-an-images/assets/93427248/6099a36b-a002-4f31-99c5-d26254a53c33)


### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![output02](https://github.com/Adithya-Siddam/Histogram-of-an-images/assets/93427248/c6cae7b9-704e-4701-bcd4-1d9d26b40335)

#### Color Image
![output03](https://github.com/Adithya-Siddam/Histogram-of-an-images/assets/93427248/86b21b5a-4cc5-4e38-b278-150fcd5dbbc5)


### Histogram Equalization of Grayscale Image.

![output04](https://github.com/Adithya-Siddam/Histogram-of-an-images/assets/93427248/d34bc5de-87c2-42cf-8459-96cb16021e35)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
