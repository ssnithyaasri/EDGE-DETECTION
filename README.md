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

 Step3:
Convert the image to grayscale

### Step4:
Using S###obel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program :

### Name: NITHYAA SRI S S
### Register No: 212222230100

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread('HOUSE.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```
![image](https://github.com/user-attachments/assets/491dbffd-1c39-4f49-950e-4c1e579e7b38)

## Sobel Edge Detection
```

# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
# Sobel Edge Detection

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/9ceb704b-9828-49d8-847b-836014680bf0)
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
plt.imshow(sobel_x, cmap='gray')
plt.title('Sobel_x')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/57498580-7f80-490d-a19f-395c53bcc186)
```
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
plt.imshow(sobel_y, cmap='gray')
plt.title('Sobel_y')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/dda2a1e7-e76f-4f9f-bdca-d26c6eb2b527)




## Laplacian Edge Detection
```

plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/95c449f4-4bbf-4b1f-a4c5-d3d39985f5e8)


## Canny Edge Detection
```

plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')

# Show all results
plt.tight_layout()
plt.show()
```
![image](https://github.com/user-attachments/assets/e1cb217f-a83e-47e2-9ed6-1bbfa45b18cb)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

