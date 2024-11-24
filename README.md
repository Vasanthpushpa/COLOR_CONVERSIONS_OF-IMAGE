# EXP-1
# COLOR_CONVERSIONS_OF-IMAGE
## AIM:
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


## Program:
### Developed By: Vasanth P
### Register Number: 212222240113


## Output:

### i)Read and Display an Image
```
import cv2
# Read the image
image = cv2.imread('lion.jpg')
# Display the image in a window
cv2.imshow('Image Window', image)
# Wait indefinitely for a key press
cv2.waitKey(0)
# Destroy all windows created by OpenCV
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/45bd776f-2bb3-49e3-a5b8-294f1ddf1364)




### ii)Draw Shapes and Add Text

```
# Load the image
image = cv2.imread('Qno. 1.jpg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

img_rgb.shape

# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)

plt.imshow(line_img, cmap='viridis')
plt.title("Image with Line")
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/ad6dddae-4a7d-40fb-a97e-808b22bcc3ee)



```
import cv2

img = cv2.imread("lion.jpg")
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10

res_img=cv2.rectangle(img,start,stop,color,thickness)

# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a6b360a2-e348-49a9-a14a-53b99d793ddb)
```
image = cv2.imread('Qno. 1.jpg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)

plt.imshow(text_img, cmap='viridis')
plt.title("Image with Text")
plt.axis('off')
plt.show()


```
![image](https://github.com/user-attachments/assets/86dc2eaf-9784-435e-b5c3-60abf002d196)

```
# Load the image
image = cv2.imread('Qno. 1.jpg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

img_rgb.shape

circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)

plt.imshow(circle_img, cmap='viridis')
plt.title("Image with Circle")
plt.axis('off')
plt.show()
```

![image](https://github.com/user-attachments/assets/0bbce7fe-1ee9-4fee-bdb3-5c73361060bc)



### iii)Image Color Conversion
```
# Load the image
image = cv2.imread('Qno. 1.jpg')

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")

# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")

# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)

# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")

# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)

# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")

# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)

plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")

```
### Convert the image from RGB to HSV and display it:
![image](https://github.com/user-attachments/assets/6d4ef807-1082-40ca-b0b4-a271ae36db73)

### Convert the image from RGB to GRAY and display it:
![image](https://github.com/user-attachments/assets/08adbbc9-8554-4c68-9dec-2e64ee3cce90)


### Convert the image from RGB to YCrCb and display it:

![image](https://github.com/user-attachments/assets/b1dfbd16-a598-417b-bf2a-c2a060857e81)


### Convert the HSV image back to RGB and display it:
![image](https://github.com/user-attachments/assets/098f061f-4bff-455d-98e2-242b0f7d72f9)


### iv)Access and Manipulate Image Pixels
```
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()

```
![image](https://github.com/user-attachments/assets/45e7c066-f460-4d5d-b666-5966ac6aede0)


### v)Image Resizing
```
# Load the image
image = cv2.imread('Qno. 1.jpg')

image.shape

# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

resized_image_rgb.shape

# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```
![image](https://github.com/user-attachments/assets/645fa9c6-d951-46f3-bc55-f89f265b5c85)


### vi)Image Cropping
```
image = cv2.imread('Qno. 1.jpg')

image.shape

# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)

# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
![image](https://github.com/user-attachments/assets/756a2e7b-609f-41d7-9b16-ec789cbfd4a8)


### vii)Image Flipping
```
# Load the image
image = cv2.imread('Qno. 1.jpg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)

# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)

# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")

# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)

# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)

# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
### Flip the original image horizontally and display it:
![image](https://github.com/user-attachments/assets/d4d22fcc-e27f-470b-8e4d-3804eb793198)


### Flip the original image vertically and display it:
![image](https://github.com/user-attachments/assets/3250de3a-54e6-473b-a2d3-2f44a02e3a86)



### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("naturek.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)


![image](https://github.com/user-attachments/assets/a0c06c12-fc84-491b-8389-1044b5311921)





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







