# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Developed By : DHARSHAN V
## Register Number: 212222230031

## INPUT /OUTPUT
## ORGINAL IMAGE
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('HappyFish.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)

# Display results using Matplotlib
plt.figure(figsize=(12, 12))

# Original Image
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![Screenshot 2024-10-28 151416](https://github.com/user-attachments/assets/cbb9c129-1b8f-4e1e-8dd9-c68223e533a6)



### SOBEL EDGE DETECTOR
```
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![Screenshot 2024-10-28 151420](https://github.com/user-attachments/assets/7ad02404-868d-4602-9dba-4763499c2fad)


### LAPLACIAN EDGE DETECTOR
```
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

```
![Screenshot 2024-10-28 151425](https://github.com/user-attachments/assets/7189880a-bf55-4d4d-b62a-a762073026b5)



### CANNY EDGE DETECTOR
```
plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')


```
![Screenshot 2024-10-28 151429](https://github.com/user-attachments/assets/3f38101e-fa51-4f1b-bb37-2752144a3e92)

```
plt.tight_layout()
plt.show()


```

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
