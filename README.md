# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Developed By

*Name:* SIVAPRASATH R

*Register No:* 212224243007

## Output

### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.


import cv2
import matplotlib.pyplot as plt
img = cv2.imread("Screenshot (227).png")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()


<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/73139755-1113-4ed4-aec0-77ddbaf51a01" />



### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.


kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()


<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/53753de4-b48d-4542-a8a6-852e6c73cd93" />



### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.


kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()


<img width="389" height="409" alt="download" src="https://github.com/user-attachments/assets/2d194681-298e-40ca-ab09-c89f5a46f847" />



## Result

Thus, the morphological operations *Erosion* and *Dilation* are successfully implemented using OpenCV.
