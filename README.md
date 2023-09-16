# IMPLEMENTATION-OF-FILTERSS
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
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.

## Program:
### Developed By   :
### Register Number:
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('thor.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')



```
ii) Using Weighted Averaging Filter
```Python



import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('thor.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```
iii) Using Gaussian Filter
```Python


import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('thor.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')


```

iv) Using Median Filter
```Python



import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('thor.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')

```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python



import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("thor.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (10,10))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("on")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernel Filtered Image")
plt.axis("on")

```
ii) Using Laplacian Operator
```Python



import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('thor.jpg')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title("Filtered")
plt.axis("off")

```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![fareed_dip1](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/1922b76f-fd44-4ba7-84d4-342536677a3b)

ii) Using Weighted Averaging Filter
![fareed_dip2](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/4d9f2d65-4cb3-42cc-bb03-7b2931468222)


iii) Using Gaussian Filter
![fareed_dip3](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/e8d7d8d4-1832-43e1-a0dc-3a645c0e3095)

iv) Using Median Filter
![fareed_dip4](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/be8824b3-5b37-4073-b8ea-0c9a48aeb001)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![fareed_dip5](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/ecd5123d-7782-4e65-ae78-3eb07c1e9568)

ii) Using Laplacian Operator

![fareed_dip6](https://github.com/MOHAMED-FAREED-22001617/IMPLEMENTATION-OF-FILTERSS/assets/121412904/341cd598-66cf-42e2-8967-434908048eb7)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
