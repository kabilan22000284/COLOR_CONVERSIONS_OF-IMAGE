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
1.Load an image from your local directory and display it.
### Step2:
1.Draw a line from the top-left to the bottom-right of the image.

2.Draw a circle at the center of the image.

3.Draw a rectangle around a specific region of interest in the image.

4.Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.Convert the image from RGB to HSV and display it.

2.Convert the image from RGB to GRAY and display it.

3.Convert the image from RGB to YCrCb and display it.

4.Convert the HSV image back to RGB and display it.

### Step4:
1.Access and print the value of the pixel at coordinates (100, 100).

2.Modify the color of the pixel at (200, 200) to white.

### Step5:
1.Resize the original image to half its size and display it.
### Step6:
1.Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.Flip the original image horizontally and display it.

2.Flip the original image vertically and display it.

### Step8:
1.Save the final modified image to your local directory.


## Program:
### Developed By: Pradeepraj P
### Register Number: 212222240073 

### i)Read and Display an Image
```
import cv2
image=cv2.imread('wallpaper.jpg',1)
image = cv2.resize(image,(500,500))
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/1de23169-5bc3-46c7-b738-5a7ceba368f6)

### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
res = cv2.line(img, (0, 0), (img.shape[1], img.shape[0]), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/90164df7-4dd4-45dd-a87f-b0093bb5ab65)

(2) Draw a circle at the center of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
height, width, _ = img.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(img, center_coordinates, 150, (255, 0, 0), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/754618e9-0ed8-44b6-bb90-b570e0fb5a45)

(3) Draw a rectangle around a specific region of interest in the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
start = (500-10,500-10)  # top-left corner of the rectangle
stop = (0+10,0+10)   # bottom-right corner of the rectangle
color = (100, 255, 100)  # Green rectangle
thickness = 10           # Thickness of the rectangle
res_img = cv2.rectangle(img, start, stop, color, thickness)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/befcdf64-d023-45b2-9fbd-94739761c519)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
text = "Opencv_drawinG"
position = (10, 50)  # Positioning the text at the top-left corner
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2
res = cv2.putText(img, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/00baeb5e-6090-4213-ab4f-c3a23bd33106)

### iii)Image Color Conversion
1) Convert the image from RGB to HSV and display it
```
img = cv2.imread('wallpaper.jpg',1)
img = cv2.resize(img,(500,500))
cv2.imshow('Original Image',img)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/95970a36-8668-486f-aa5e-7368c22a10bb)

(2) Convert the image from RGB to GRAY and display it.
```
img = cv2.imread('wallpaper.jpg',1)
img = cv2.resize(img,(400,400))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/e450b0fa-f4c5-4078-a4a8-80617918ab35)

3) Convert the image from RGB to YCrCb and display it.
```
img = cv2.imread('wallpaper.jpg',1)
img = cv2.resize(img,(400,400))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/6ffaece3-e442-40ad-9da5-bb438642bf7b)

(4) Convert the HSV image back to RGB and display it.
```
img = cv2.imread('wallpaper.jpg',1)
img = cv2.resize(img,(400,400))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/ddc827eb-c6ca-4203-9855-f3cd365576da)

### iv)Access and Manipulate Image Pixels
```
img = cv2.imread('wallpaper.jpg', 1)
img = cv2.resize(img, (400, 400))
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255]  # Setting the pixel value to white (BGR)
cv2.imshow('Modified Image', img)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/f4513f72-2d9e-4faf-a83d-020d14102dd1)

### v)Image Resizing
```
img = cv2.imread('wallpaper.jpg', 1)
resized_img = cv2.resize(image, (400, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/fbbe8f32-2116-406e-ac83-ea61cf50c2e8)

### vi)Image Cropping
```
image1=cv2.imread('wallpaper.jpg',1)
x, y = 50, 50
width, height = 425, 425
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/07012821-42a8-4aad-b3ea-59890f552611)

### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(400,400))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/021ea332-4c8d-46af-b5a4-3df248e1e5b8)

(2) Flip the original image vertically and display it.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(400,400))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
# Display the HSV image
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![image](https://github.com/user-attachments/assets/2d7ebe52-7ef3-4614-83fa-3391c6394273)

### viii)Write and Save the Modified Image
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(300,300))
cv2.imwrite('sipder_man.jpg',img)
```
### Output
![image](https://github.com/user-attachments/assets/c6d3d7e9-5b66-48de-94d8-f517ab6ff2e3)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







