## Record-Implementation-of-Filters

## Image Smoothing and Sharpening Using OpenCV:

## Aim:

To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.


## The program performs the following operations:

* Read and display an input image
* Apply Averaging filter
* Apply Weighted Averaging filter
* Apply Gaussian filter
* Apply Median filter
* Apply Laplacian sharpening using kernel
* Apply Laplacian operator
* Display all outputs for comparison

## Software Used:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm:

## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Read the input image (e.g., image.jpg).

## Step 3:
Convert the image from BGR to RGB format for display.

## Step 4:
Apply Averaging Filter using cv2.blur().

## Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

## Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

## Step 7:
Apply Median Filter using cv2.medianBlur().

## Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

## Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

## Step 10:
Display all filtered images using a grid layout for comparison.

## Program:

## Developed By : SARAN RAJ M

## Register No : 212225240138

## Smoothing Filters:

## Averaging Filter Image:

```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("sai1.jpeg")
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

## Weighted Averaging Filter Image:

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

## Gaussian Blur:

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

## Median Blur:

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

## Sharpening Filters:

## Laplacian kernel:

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

## Laplacian Operator:

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

## Output:

## Smoothing Filters:

## Original Image And Averaging Filter Image:

<img width="600" height="217" alt="image" src="https://github.com/user-attachments/assets/168a7fe1-af04-471b-95fe-25a960fff0bb" />


## Original Image And Weighted Averaging Filter Image:

<img width="485" height="163" alt="image" src="https://github.com/user-attachments/assets/ae5db7db-7ec5-46b7-9c91-745cdc6f7212" />


## Original Image And Gaussian Blur:

<img width="430" height="162" alt="image" src="https://github.com/user-attachments/assets/49831cec-c99c-4490-aacd-b9e26fa8aed0" />


## Original Image And Median Blur:
<img width="595" height="207" alt="image" src="https://github.com/user-attachments/assets/39805b54-fca6-451b-896e-7265751f40cc" />


## Sharpening Filters:

## Original Image And Laplacian kernel:

<img width="471" height="167" alt="image" src="https://github.com/user-attachments/assets/79207eae-951b-4269-97ca-353b018edcde" />


## Original Image And Laplacian Operator:

<img width="435" height="158" alt="image" src="https://github.com/user-attachments/assets/d289a546-a05d-408a-b3e1-f025d1ab315d" />


## Result:

Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.

The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.
