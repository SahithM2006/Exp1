# Image-Handling-and-Pixel-Transformations-Using-OpenCV
# AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
# Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)
# Algorithm:
Step 1:
Load an image from your local directory and display it.

Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

Program Developed By:
Name: [Your Name Here]

Register Number: [Your Register Number Here]

Ex. No. 01


Ex 1: Image Handling and Pixel Transformations Using OpenCV
Name: SAHITH M
Reg no: 212224230236

import cv2
import matplotlib.pyplot as plt
# Read the image using OpenCV
```
img = cv2.imread('images.jpg', cv2.IMREAD_COLOR)
```
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
# Display the image using Matplotlib
```
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/78c07061-bbb0-4e0a-8a01-b2ca716f4373" />

# Load the image
```
image = cv2.imread('images.jpg')
``` 
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(554, 554, 3)
```
# Draw a line from top-left to bottom-right
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('on')  
plt.show()
```
<img width="425" height="433" alt="image" src="https://github.com/user-attachments/assets/d262a845-acb7-4fc9-8df3-e61aec683de3" />

# Load the image
```
image = cv2.imread('images.jpg') 
```
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(554, 554, 3)
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/cb143042-14e7-49d0-abaa-2a5324ed8f08" />

# Load the image
```
image = cv2.imread('images.jpg') 
```
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
(554, 554, 3)
```
# Draw a rectangle around the Whole image
```
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/07c6afa0-124b-4b4b-a9a1-26989b12cc8d" />

# Load the image
```
image = cv2.imread('images.jpg') 
```
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
# Add text to the image
```
text_img = cv2.putText(img_rgb, "Sahith Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/8900c04f-04be-44dd-9968-08f9ba1e7c4a" />

# Load the image
```
image = cv2.imread('images.jpg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
# Original RGB Image
```
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/be1919ab-d30c-438e-a516-65c778b4be29" />

# Convert RGB to HSV
```
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
```
# HSV Image
```
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/2b3cd9a3-c27e-4a1f-90d1-181114e26c29" />

# Convert RGB to GRAY
```
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
```
# Grayscale Image
```
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/b43d0361-f889-46d7-a27c-d40ff5b090c0" />

# Convert RGB to YCrCb
```
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
```
# YCrCb Image
```
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/e3f5eac2-2fb9-4c5f-8f4a-9516d8e99b36" />

# Convert HSV back to RGB
```
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/9dc4d331-443f-4597-ba6c-37be5d7586e7" />

# Modify a block of pixels (300x300) to white, starting from (200, 200)
```
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
```
# Convert BGR to RGB for displaying with Matplotlib
```
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
# Display the modified image
```
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/0263d32a-9bb5-4b83-959d-7446828f8d51" />

# Load the image
```
image = cv2.imread('images.jpg') 
image.shape
(554, 554, 3)
```
# Resize the image to half its size
```
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
```
# Convert BGR to RGB for displaying with Matplotlib
```
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
(300, 384, 3)
```
# Display the resized image
```
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
<img width="493" height="409" alt="image" src="https://github.com/user-attachments/assets/02fd0595-f047-4040-b034-a5d01ac02f23" />

# Load the image
```
image = cv2.imread('images.jpg') 
image.shape
(554, 554, 3)
```
# Crop a 300x300 region starting from (50, 50)
```
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349
```
# Convert BGR to RGB for displaying with Matplotlib
```
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
```
# Display the cropped region (ROI)
```
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/408383a2-ff5b-43c9-a1c0-d39f17bed455" />

# Load the image
```
image = cv2.imread('images.jpg')
```
# Flip the image horizontally (left-right)
```
flipped_horizontally = cv2.flip(image, 1)
```
# Convert BGR to RGB for displaying with Matplotlib
```
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
```
# Horizontal flip
```
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/1ccfc7cd-8059-4142-9b22-a89d0cecc387" />

# Flip the image vertically (up-down)
```
flipped_vertically = cv2.flip(image, 0)
```
# Convert BGR to RGB for displaying with Matplotlib
```
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
```
# Vertical flip
```
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
(np.float64(-0.5), np.float64(553.5), np.float64(553.5), np.float64(-0.5))
```
<img width="389" height="409" alt="image" src="https://github.com/user-attachments/assets/584b8828-a857-4a10-b96a-900806096093" />

# Output:
i) Read and Display an Image.
ii) Adjust Image Brightness.
iii) Modify Image Contrast.
iv) Generate Third Image Using Bitwise Operations.
# Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.
