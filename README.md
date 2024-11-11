# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale

### Step3:
Use Global thresholding to segment the image

### Step4:
 Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image and display results.

## Program
### Name:VIjayaraj V
### Register number:212222230174
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Otsu's thresholding
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

# Display the Otsu thresholding result
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()

# Read the Image and convert to grayscale
image = cv2.imread('central.jpg')

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(image)
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
                                    cv2.THRESH_BINARY, 11, 2)
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()



# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()


```
## Output

### Original Image
![Screenshot 2024-10-09 152155](https://github.com/user-attachments/assets/3d9c977d-7497-4d56-bc97-4af7faa7a821)

### Global Thresholding
![Screenshot 2024-10-09 152204](https://github.com/user-attachments/assets/da15091c-a99f-4f51-a786-cf5d49a304ef)


### Adaptive Thresholding
![Screenshot 2024-10-09 152217](https://github.com/user-attachments/assets/db53c801-6fc4-4389-bd1d-b5192ea2c014)


### Optimum Global Thesholding using Otsu's Method
![Screenshot 2024-10-09 152225](https://github.com/user-attachments/assets/7c60be68-0fa1-4749-aea2-fa16b92f954d)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
