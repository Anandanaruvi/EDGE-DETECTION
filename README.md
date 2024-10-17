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

## Program and Output:
```python
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread('beautifulflower.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

![image](https://github.com/user-attachments/assets/244d5090-f9e1-4363-bbff-8d1e13fbae70)

### SOBEL EDGE DETECTOR
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined)
plt.title('sobel combined image')
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/ce6194b6-bcf0-4714-9e45-bb64898f469e)


### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian)
plt.title('Laplacian image')
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/28c1c1fc-9adf-4992-bc11-52fbee613fbe)



### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges)
plt.title('canny_edges Image')
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/83b38edf-71d8-4f7f-90bb-75563bae5c0b)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.

