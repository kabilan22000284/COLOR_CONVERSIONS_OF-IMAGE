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
### Developed By: Kabilan V
### Register Number: 212222100018

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
![download](https://github.com/user-attachments/assets/535a7f2e-3e25-491d-8df1-3239b79aab29)

### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
res = cv2.line(img, (0, 0), (500,500), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![download](https://github.com/user-attachments/assets/17ed7fb9-9370-43a6-af7e-f0babbc9e9ef)

(2) Draw a circle at the center of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
res = cv2.circle(img,(250,250), 150, (255, 0, 0), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![download](https://github.com/user-attachments/assets/a8362048-f9a2-4afb-8373-7fecca877a30)

(3) Draw a rectangle around a specific region of interest in the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
res_img = cv2.rectangle(img, (500-10,500-10), (0+10,0+10),(100, 255, 100), 10)
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows())
```
### Output
![download](https://github.com/user-attachments/assets/e6f4796a-e62b-4b3b-ad1d-bd01e1e73620)

(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
img = cv2.imread("wallpaper.jpg")
img = cv2.resize(img,(500,500))
font = cv2.FONT_HERSHEY_SIMPLEX
res = cv2.putText(img,"Opencv_drawinG", (10,50), font,1, (255, 255, 255),2)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![download](https://github.com/user-attachments/assets/4dc5ed2d-dad8-423e-b587-6c8de0d1d4d4)

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
![download](https://github.com/user-attachments/assets/7b52a538-e18f-4e08-b1c9-a2fe13446077)

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
![download](https://github.com/user-attachments/assets/2614198f-0d0f-4131-b4d9-6fc9aa55b56d)

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
![download](https://github.com/user-attachments/assets/90c98ce6-89da-40da-8a35-601ee8570319)

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
![download](https://github.com/user-attachments/assets/1dd00366-699d-4fbd-93f5-9ea2c0385edb)

### iv)Access and Manipulate Image Pixels
```
img = cv2.imread('wallpaper.jpg', 1)
img = cv2.resize(img, (400, 400))
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255]
cv2.imshow('Modified Image', img)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![download](https://github.com/user-attachments/assets/a0047552-ca4e-4cbd-9a97-7cf881dfd588)

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
![download](https://github.com/user-attachments/assets/f4eef2e6-fb79-4ae5-a363-be049cb4e00b)

### vi)Image Cropping
```
image1=cv2.imread('wallpaper.jpg',1)
roi = image1[50:50 + 425, 50:50 + 425]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output
![download](https://github.com/user-attachments/assets/16407666-df00-48c1-990a-fd1cb261d57b)

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
![download](https://github.com/user-attachments/assets/5db2393e-cf03-4478-a1d3-1ff433db286d)

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
![download](https://github.com/user-attachments/assets/34eae9e3-76cc-462d-a397-1ccfc6e69b3c)

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







