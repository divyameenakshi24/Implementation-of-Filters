# Implementation-of-Filters
## AIM:
To implement filters for smoothing and sharpening the images in the spatial domain.
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1:
Import the necessary modules. 
### Step 2:
For performing smoothing operation on a image. 
- Average filter
```python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
- Weighted average filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
- Gaussian Blur 
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
- Median filter
```python
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.
- Laplacian Kernel
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
- Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.
## PROGRAM:
```python
# Developed By   : A.DIVYA MEENAKSHI 
# Register Number: 212220230014

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("j.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters
i) Using Averaging Filter
```Python
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
```Python
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
```Python
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
```Python
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
```Python
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
```Python
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

i) Using Averaging Filter

![1](https://user-images.githubusercontent.com/75235402/167811956-91a41ffd-2f2e-4e8d-bfd8-b6acdb7a02cc.jpg)




ii) Using Weighted Averaging Filter

![2](https://user-images.githubusercontent.com/75235402/167811972-972c887e-f833-468d-89fb-6cacf9331249.jpg)




iii) Using Gaussian Filter


![3](https://user-images.githubusercontent.com/75235402/167812004-ca6f6a60-c9c8-4477-bdb5-903fcfc6fded.jpg)



iv) Using Median Filter
![4](https://user-images.githubusercontent.com/75235402/167812043-4cc406d4-fc36-4cb3-83d6-c4ed25a75cda.jpg)



### 2. Sharpening Filters

i) Using Laplacian Kernal


![Screenshot 2022-05-11 142902](https://user-images.githubusercontent.com/75235402/167812074-96a895e2-0a90-4d07-9fd1-97b7f4918015.jpg)



ii) Using Laplacian Operator

![5](https://user-images.githubusercontent.com/75235402/167812133-3baefcd6-2b36-4dd3-bf28-2fb41a4ea0bb.jpg)





## RESULT:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
