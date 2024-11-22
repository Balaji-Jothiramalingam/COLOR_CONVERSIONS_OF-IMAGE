## COLOR_CONVERSIONS_OF-IMAGE
# AIM
Write a Python program using OpenCV that performs the following tasks:

 i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii) Write and Save the Modified Image

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Load an image from your local directory and display it.

## Step2:
Draw a line from the top-left to the bottom-right of the image.

Draw a circle at the center of the image.

Draw a rectangle around a specific region of interest in the image.

Add the text "OpenCV Drawing" at the top-left corner of the image.

## Step3:
Convert the image from RGB to HSV and display it.
Convert the image from RGB to GRAY and display it.
Convert the image from RGB to YCrCb and display it.
Convert the HSV image back to RGB and display it.
## Step4:
Access and print the value of the pixel at coordinates (100, 100).
Modify the color of the pixel at (200, 200) to white.
## Step5:
Resize the original image to half its size and display it.

## Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.

## Step7:
Flip the original image horizontally and display it.
Flip the original image vertically and display it.
Step8:
Save the final modified image to your local directory.

## Developed By:BALAJI J
## Register Number: 212221243001
## Program & Output:
## i)Read and Display an Image

## Load an image from your local directory and display it.
```
import cv2 
image=cv2.imread('forest.png',1)
image =cv2.resize(image, (400, 300))
cv2.imshow('WINDOW',image)
cv2.waitKey(0)
cv2.destroyAllW

```
![365697377-8e2c2ec1-6f92-4d56-9e03-f77c7babfd9f](https://github.com/user-attachments/assets/9fb8684f-bc49-4538-8421-54e12c72fb60)
indows()

## ii)Draw Shapes and Add Text
## (1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image, (400, 300))
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


![365697526-e17d698d-4b12-4734-ba4e-2da2f1b85f5c](https://github.com/user-attachments/assets/25cf7759-c48f-40d8-9c65-bdb161adb311)

## (2) Draw a circle at the center of the image.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image, (400, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365692949-091b9155-2bc7-4632-9be0-9d30aff022ed](https://github.com/user-attachments/assets/32f08a61-0330-48ed-886d-b531769d74d6)

## (3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image, (400, 300))
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

![365693069-49e51559-40d8-46cf-bc9f-3b0bd420c25f](https://github.com/user-attachments/assets/d9e23b1a-623b-41e2-9432-76cca25bb1fd)



## (4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image, (400, 300))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365693335-f295f325-3e09-4ddc-8fec-614217b2338c](https://github.com/user-attachments/assets/22b45c38-4793-4800-b06a-910db3066d42)

## iii)Image Color Conversion
## (1) Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/5c04025a-98e0-4500-a07e-eeb92bca9be7)


![365693756-79512306-b4fd-480f-902c-23844d4a883a](https://github.com/user-attachments/assets/03b97ee9-4747-40e4-b902-72c6d3a943f3)

## (2) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/7abe661f-7474-4ead-8b60-5ba538d14f9f)


![365693960-1a99ef6f-abce-408c-a4ce-b224c83d8613](https://github.com/user-attachments/assets/4ec2574b-8939-4978-91d4-045de6c98182)


## 3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/45d714f3-8399-475e-97bd-4f407994ce0b)

![365694179-cd1fe6a9-e3f7-4fe9-8784-6de96635a498](https://github.com/user-attachments/assets/00b08b98-a022-40e0-8ed5-06af2fcb485f)

## (4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
```
![365694432-c8563dcc-761e-48e6-8b80-8953a3a18ad8](https://github.com/user-attachments/assets/a5f780df-e09e-4d34-b3c3-87c1faf932ce)



![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/6e676878-9043-4bd4-b31e-c8d3c3873d15)


## v)Access and Manipulate Image Pixels
## (1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
Screenshot 2024-09-09 142011
```
## (2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


![365698462-1ec49499-e63f-43b2-9193-2f8215d56edc](https://github.com/user-attachments/assets/5bf8639d-b856-4d62-a011-31c3a6a93a2f)

![365695725-56679372-51da-4f5d-aba7-057d5fa6eb9a](https://github.com/user-attachments/assets/b179a921-0e3b-4903-b085-0708aefe081a)

## v)Image Resizing
# Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/68897046-cf8c-430f-a01c-858b0e909cda)


## vi)Image Cropping
## Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```

import cv2
image = cv2.imread('forest.png',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


![365696216-f7b7078c-97d8-46b2-b466-38d315e6df65](https://github.com/user-attachments/assets/d0a022b7-5f47-4ee6-8b0b-f5b132518403)
## vii)Image Flipping
## (1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows(
```
![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/f09457f0-9bb7-44f3-8673-62a743b6e933)

![365696504-994b3925-39c2-4a6f-8ad0-b239a9dd0e05](https://github.com/user-attachments/assets/8675f65a-c32a-4bc6-bddc-7957aec49322)



## (2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("forest.png")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![365693576-dfa6a444-c37d-402d-91f5-5f4684addf22](https://github.com/user-attachments/assets/b121ab01-628a-44d6-9405-1dbf43074ce1)

![365696688-0b876746-51f5-443e-b02a-882f52918b26](https://github.com/user-attachments/assets/1da0785e-b81a-491b-a035-5fd7da3e38af)

## viii)Write and Save the Modified Image
## Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("forest.png")
img = cv2.resize(img,(300,200))
cv2.imwrite('boat_pic.jpg',img)


```
![365696833-80cc4672-5bb4-449a-b297-133795cbf111](https://github.com/user-attachments/assets/81db3002-4918-407a-9f89-5fe283f05203)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.
