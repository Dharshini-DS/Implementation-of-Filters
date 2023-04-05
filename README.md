# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1: 
Import the necessary modules.

### Step 2: 
For performing smoothing operation on a image.

### Step 3:
Average filter kernel=np.ones((11,11),np.float32)/121 image3=cv2.filter2D(image2,-1,kernel)

### Step 4:
Weighted average filter kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16 image3=cv2.filter2D(image2,-1,kernel1)

### Step 5:
Gaussian Blur gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)

### Step 6:
Median filter median=cv2.medianBlur(image2,13) Step 3: For performing sharpening on a image.

### Step 7:
Laplacian Kernel kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]]) image3=cv2.filter2D(image2,-1,kernel2) Laplacian Operator laplacian=cv2.Laplacian(image2,cv2.CV_64F) Step 4: Display all the images with their respective filters.

## Program:
### Developed By   : Dharshini D.S
### Register Number: 212221230022

### 1. Smoothing Filters
i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Fawzil.jfif")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
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
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
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

iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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
</br>

i) Using Averaging Filter

![output](./1.png)
</br>

ii) Using Weighted Averaging Filter

![output](./2.png)
</br>

iii) Using Gaussian Filter

![output](./3.png)
</br>

iv) Using Median Filter

![output](./4.png)
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![output](./5.png)
</br>

ii) Using Laplacian Operator

![output](./6.png)
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
