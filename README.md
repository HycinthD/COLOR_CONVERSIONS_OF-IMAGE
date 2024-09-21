# COLOR_CONVERSIONS_OF-IMAGE
## AIM
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


##### Program:
### Developed By:HYCINTH D
### Register Number: 212223240055


## Output:

### i)Read and Display an Image
i.Load an image from your local directory and display it.
```
import cv2
image=cv2.imread('lokesh.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/75de2c2d-4648-45e9-9150-545c910743fd)


### ii)Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
img = cv2.imread("lokesh.JPG")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/938b4873-594c-4028-8091-f007cc4b2121)

2.Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("lokesh.jpg")
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 150, (255,0, 0), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d9cad402-c391-4795-8eac-d754f254aef5)

3.Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("lokesh.JPG")
start=(0,0)
stop=(689,389)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(image,start,stop,color,thickness)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/67e0786e-2427-43ae-b2f8-5c9a88f0b4a7)

4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```

import cv2
img = cv2.imread("lokesh.JPG")
text = "OPENCV DRAWING"
position = (50, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/5d6e32eb-be23-4de5-8e31-7e728d82f3fa)

### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/51e1a598-bbfa-460b-9342-bb9e29576f70)

(2) Convert the image from RGB to GRAY and display it.
```
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/17e22465-d819-4fca-83e6-e0e511ae3702)

(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/04017b63-ceb7-4484-9b96-c3d7d9cb6ffb)

(4) Convert the HSV image back to RGB and display it.
```
import cv2
img = cv2.imread('lokesh.jpg',1)
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/73f4c5c7-1ecd-4c7d-b5e5-e9799f348c10)

### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
import cv2
img = cv2.imread('lokesh.jpg', 1)
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255] 
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f766d853-eecc-44d5-95b6-557de8c917b1)

### v)Image Resizing
Resize the original image to half its size and display it.
```
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(image, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
![image](https://github.com/user-attachments/assets/164e4f8e-64d2-42d8-bae7-338419224a59)

### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image1=cv2.imread('lokesh.jpg',1)
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/bdf43a06-5718-46d4-9005-010521c518ba)

### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/12435b16-42a7-4a4c-8f79-893e3f7f7fa9)
(2) Flip the original image vertically and display it.
```
import cv2

img = cv2.imread("lokesh.JPG")
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/b1b58a12-a76e-48fb-8804-b9f4493bc22b)


### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("lokesh.JPG")
cv2.imwrite('lokesh1.jpg',img)
```
![image](https://github.com/user-attachments/assets/a3745440-01b0-48de-8448-ee26002c85c2)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







