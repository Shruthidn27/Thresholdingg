# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm
## Step1:
Load the necessary packages.

## Step2:
Read the Image and convert to grayscale.

## Step3:
Use Global thresholding to segment the image.

## Step4:
Use Adaptive thresholding to segment the image.

## Step5:
Use Otsu's method to segment the image and display the results.

## Program

```python
# Name: Shruthi D N
# Reg no: 212223240155
# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt




# Read the Image and convert to grayscale
image = cv2.imread("D:\DIPT\images (1).jpg")  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  # Convert to grayscale
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')





# Use Global thresholding to segment the image
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)




# Use Adaptive thresholding to segment the image
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)



# Use Otsu's method to segment the image 
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)




# Display the results
# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()




```
## Output

### Original Image
<img width="870" height="310" alt="image" src="https://github.com/user-attachments/assets/4aa144fb-f58f-4e2b-bdc5-6754c84811fa" />


### Global Thresholding
<img width="853" height="311" alt="image" src="https://github.com/user-attachments/assets/ce91659b-79b3-485e-8eac-baecf01a62b9" />


### Adaptive Thresholding
<img width="821" height="289" alt="image" src="https://github.com/user-attachments/assets/430a13e4-3fb6-450f-bbf4-a8db75ff3887" />


### Optimum Global Thesholding using Otsu's Method



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
