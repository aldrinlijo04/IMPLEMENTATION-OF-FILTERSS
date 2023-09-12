# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
</br>
</br> 

### Step2
Convert the image from BGR to RGB.
</br>
</br> 

### Step3
Apply the required filters for the image separately.
</br>
</br> 

### Step4
Plot the original and filtered image by using matplotlib.pyplot
</br>
</br> 

### Step5
End the program.
</br>
</br> 

## Program:
### Developed By   : ALDRIN LIJO J E
### Register Number: 212222240007
</br>

### 1. Smoothing Filters
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("a.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```

### i) Using Averaging Filter
```
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

### ii) Using Weighted Averaging Filter
```
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

### iii) Using Gaussian Filter
```
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

### iv) Using Median Filter
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

### i) Using Laplacian Kernal
```
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

### ii) Using Laplacian Operator
```
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
## 1. Smoothing Filters

</br>

## i) Using Averaging Filter
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/0c3d5d82-0e58-4efc-8cf9-c8d9a2a70388)

</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

## ii) Using Weighted Averaging Filter
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/cf6d8073-b160-4853-9d15-f58dcd6f5284)

</br>
</br>
</br>

## iii) Using Gaussian Filter
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/9283aed3-cbae-4ea5-b9c7-00967958f598)
</br>
</br>
</br>

## iv) Using Median Filter
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/632457d5-b675-4e20-bf20-9016a049e6e0)
</br>
</br>
</br>

## 2. Sharpening Filters

</br>

## i) Using Laplacian Kernal
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/d69a9a30-8ece-4b6e-bd34-a7044cb2ba96)

</br>
</br>
</br>

## ii) Using Laplacian Operator
![download](https://github.com/aldrinlijo04/IMPLEMENTATION-OF-FILTERSS/assets/118544279/1de13591-1301-4821-b9e9-f2f43977e1b4)

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
