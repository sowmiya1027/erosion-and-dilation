# Exp 9: IMPLEMENTATION OF EROSION AND DILATION USING OPENCV
# Name: Sowmiya R
# Reg No: 212225040420

## AIM

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

## SOFTWARE REQUIRED

- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook
- Anaconda (optional)

## INSTALLATION

Install the required libraries using the following command:

```bash
pip install opencv-contrib-python-headless numpy matplotlib
```

## ALGORITHM

### Step 1: Import Libraries
- Import OpenCV for image processing.
- Import NumPy for creating and manipulating images.
- Import Matplotlib for displaying images.

### Step 2: Create a Blank Image
- Create a blank image using NumPy.
- Initialize the image with a black background.

### Step 3: Insert Text
- Add text to the blank image using `cv2.putText()`.
- Display the text image.

### Step 4: Create a Kernel
- Create a structuring element using `cv2.getStructuringElement()`.
- Specify a suitable kernel size for morphological operations.

### Step 5: Perform Image Erosion
- Apply erosion using `cv2.erode()`.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 6: Perform Image Dilation
- Apply dilation using `cv2.dilate()`.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 7: Compare the Results
- Display the original input image.
- Display the eroded image.
- Display the dilated image.
- Observe the differences between the three images.

## PROGRAM
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Sowmiya R', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```

## OUTPUT

The following outputs are obtained:

### 1. Input Image
<img width="670" height="442" alt="image" src="https://github.com/user-attachments/assets/6b435821-cac2-459c-b0e5-356115f8131e" />


### 2. Eroded Image
<img width="577" height="443" alt="image" src="https://github.com/user-attachments/assets/29a45182-c4a5-4e59-8a6a-2f42a15a2e47" />


### 3. Dilated Image
<img width="572" height="422" alt="image" src="https://github.com/user-attachments/assets/51e53582-25f9-4887-b288-73ac43c02c0d" />


## RESULT

Thus, the morphological operations Erosion and Dilation were successfully implemented using Python and OpenCV. The input, eroded, and dilated images were displayed and compared.
