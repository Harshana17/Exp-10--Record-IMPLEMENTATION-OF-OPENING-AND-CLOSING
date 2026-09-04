# Opening and Closing Operations Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological Opening and Closing operations on an image.

The program performs the following operations:

- Morphological Opening
- Morphological Closing

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

Create or load an input image containing foreground objects.

### Step 3:

Display the original image.

### Step 4:

Create a structuring element (kernel) of suitable size.

### Step 5: Opening Operation

- Apply the Opening operation using the structuring element.
- Opening consists of Erosion followed by Dilation.
- Remove small foreground noises while preserving the shape of larger objects.
- Display the opened image.

### Step 6: Closing Operation

- Apply the Closing operation using the structuring element.
- Closing consists of Dilation followed by Erosion.
- Fill small holes and gaps within foreground objects.
- Display the closed image.

### Step 7:

Compare the original, opened, and closed images.

## Program

## Developed By

**Name:** HARSHANA M V

**Register No:** 212224240053

## ORIGINAL IMAGE

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = np.zeros((400, 600), dtype=np.uint8)

cv2.putText(img, "HARSHANA M V", (80, 200),
            cv2.FONT_HERSHEY_SIMPLEX, 1.5, 255, 3)

kernel = np.ones((5, 5), np.uint8)

opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel)

closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel)

plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap="gray")
plt.title("Original")
plt.axis("off")
```
<img width="368" height="278" alt="image" src="https://github.com/user-attachments/assets/58be33a5-4ce8-4503-a59e-862c6f6d7ffa" />

## OPENING IMAGE

```
plt.subplot(1, 3, 2)
plt.imshow(opening, cmap="gray")
plt.title("Opening")
plt.axis("off")

```
<img width="216" height="176" alt="image" src="https://github.com/user-attachments/assets/5380039b-622e-42b8-8afc-4883e858c5cf" />

## CLOSING IMAGE

```
plt.subplot(1, 3, 3)
plt.imshow(closing, cmap="gray")
plt.title("Closing")
plt.axis("off")
plt.show()
```
<img width="218" height="161" alt="image" src="https://github.com/user-attachments/assets/8a90014c-44ae-4e16-a5e2-01b8c2b41278" />

## COMPARIOSN OF ALL THREE
```
plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(opening, cmap="gray")
plt.title("Opening")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(closing, cmap="gray")
plt.title("Closing")
plt.axis("off")

plt.show()
```
<img width="1196" height="282" alt="image" src="https://github.com/user-attachments/assets/5023b94c-f30e-4ac8-b3cb-9fca372eb550" />

## Applications

### Opening

- Noise removal in binary images.
- Separation of connected objects.
- Preprocessing for object detection.

### Closing

- Filling small holes in objects.
- Connecting nearby components.
- Enhancing segmented regions.

## Advantages

### Opening

- Removes unwanted foreground noise.
- Preserves major object structures.
- Improves segmentation quality.

### Closing

- Restores object continuity.
- Eliminates small background gaps.
- Improves object representation.

## Result

Thus, the morphological operations **Opening** and **Closing** are successfully implemented using OpenCV. 
