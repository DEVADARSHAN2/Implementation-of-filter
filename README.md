# Implementation-of-filter
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
### Developed By   : DEVADARSHAN A S
### Register Number: 212222110007
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("cad.jpeg")
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
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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
![Screenshot 2024-03-19 143723](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/f458aacd-377e-44f7-80a6-595102f3ef02)


ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 143734](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/98df351b-196a-49ce-9db8-55b48b694181)

iii) Using Gaussian Filter

![Screenshot 2024-03-19 143740](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/4f15808c-ec5f-4e8e-b36a-7ff37d373029)

iv) Using Median Filter

![Screenshot 2024-03-19 143748](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/22fd1fec-1e5c-4701-86e0-f4d1c516857d)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-19 143756](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/757802db-014a-47a0-bfc3-660d422f22c8)

ii) Using Laplacian Operator

![Screenshot 2024-03-19 143803](https://github.com/DEVADARSHAN2/Implementation-of-filter/assets/119432150/21b6646d-215c-4abe-9401-8574e4506a20)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
