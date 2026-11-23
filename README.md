## Lane Detection
## Aim
To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

## Learning Objective
Understand each stage of image processing
Learn how to build a complete computer vision pipeline
Practice writing code in guided sections
Important Instruction: 👉 Write code ONLY in places marked as # Your Code Here 👉 Do NOT modify any other part of the code

## Software Used
- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib
## Algorithm & Explanation
Developed By
Name:Kruthika R
Register No: 212225240075

## Program

## 1.Import Libraries
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## 2.Read the Image
```
img = cv2.imread('road.jpg')
```
## 3.Convert to Grayscale
```
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
```
## 4.Display Images
```
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

plt.show()
```
## 5.Thresholding
```
threshold = cv2.threshold(gray, 150, 255, cv2.THRESH_BINARY)[1]
```
## 6.Region of Interest (ROI)
ROI masking already provided
(Do not modify)

## 7.Edge Detection (Canny)
```
edges = cv2.Canny(gray, 50, 150)
```

## 8.Gaussian Blur
```
blur = cv2.GaussianBlur(edges, (5, 5), 0)
```
## 9.Hough Transform
```
lines = cv2.HoughLinesP(
    blur,
    rho=1,
    theta=np.pi/180,
    threshold=50,
    minLineLength=50,
    maxLineGap=100
)
```
## Lane Detection Logic
Already implemented
(Do not modify)

## Output

## Original image
<img width="1280" height="720" alt="EXP7" src="https://github.com/user-attachments/assets/17766ebc-b75a-4ebb-861d-28923d78cd14" />

## Grayscale image
<img width="748" height="412" alt="image" src="https://github.com/user-attachments/assets/9178b1b5-4e55-4c30-b206-395913410a11" />

## Thresholding
<img width="982" height="551" alt="image" src="https://github.com/user-attachments/assets/a28a1bc6-08a5-46ee-bf60-e0d08d248337" />

## Edge Detection
<img width="1190" height="657" alt="image" src="https://github.com/user-attachments/assets/0bb8cba4-9a17-45d5-a510-106b878e05a0" />

## Detected lines
<img width="1166" height="692" alt="image" src="https://github.com/user-attachments/assets/65cebcac-ef75-4780-a6ce-d793daad47b7" />

## Final line detection
<img width="1391" height="797" alt="image" src="https://github.com/user-attachments/assets/8d5d72d3-6592-441d-9024-f17fa1ab89fb" />

## Result
Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

