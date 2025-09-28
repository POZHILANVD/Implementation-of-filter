# Implementation-of-filter
### NAME : POZHILAN V D
### REG NO : 212223240118
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.


### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.

### Step5
End the program.
## Program:
```
 Developed By   : POZHILAN V D
 Register Number: 212223240118
```

### 1. Smoothing Filters

## i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Imgage2.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
## iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
## iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
## i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()





```
## ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters

## i) Using Averaging Filter
<img width="1013" height="509" alt="image" src="https://github.com/user-attachments/assets/8c51b6c5-4445-4405-a158-64128e87d92d" />


## ii)Using Weighted Averaging Filter
<img width="749" height="384" alt="image" src="https://github.com/user-attachments/assets/320bc049-0e23-4dc2-a887-22c398560dce" />


## iii)Using Gaussian Filter
<img width="732" height="381" alt="image" src="https://github.com/user-attachments/assets/e19bd5ef-562c-4468-8214-4ba843d5e6a8" />

## iv) Using Median Filter
<img width="1006" height="507" alt="image" src="https://github.com/user-attachments/assets/2fe7a916-86ff-4982-92c5-35258c972bc8" />


### 2. Sharpening Filters


## i) Using Laplacian Kernal

<img width="724" height="391" alt="image" src="https://github.com/user-attachments/assets/609eff92-1284-450b-ac70-2c7f74560433" />

## ii) Using Laplacian Operator
<img width="725" height="363" alt="image" src="https://github.com/user-attachments/assets/96659c6f-5200-47c1-8a45-f8f976e49683" />

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
