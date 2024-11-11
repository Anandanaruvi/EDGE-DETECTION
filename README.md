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
image = cv2.imread('fish.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

![image](https://github.com/user-attachments/assets/3f902242-aa0d-410a-8a8e-0452d6165822)


### SOBEL EDGE DETECTOR
```python
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions

plt.imshow(sobel_combined)
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/62020b0a-6d32-428f-a489-256471b3341e)



### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian)
plt.title('Laplacian image')
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/34f72aaf-51cc-4ad2-9133-581d7951dc63)


### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges)
plt.title('canny_edges Image')
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/8638403a-2d71-4fa0-9e90-93bea76fd737)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.


