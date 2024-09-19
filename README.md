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
### Developed By: Vinush.CV
### Register Number: 212222230176


## Output:

### i)Read and Display an Image

```python
import cv2
image = cv2.imread('gpro.jpg')
# Display the image in a window
cv2.imshow('Image Window', image)
# Wait indefinitely for a key press
cv2.waitKey(0)
# Destroy all windows created by OpenCV
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/9144db59-8670-42cc-95de-f973bbbd19ea)


### ii)Draw Shapes and Add Text

#### 1) Draw a diagonal line:
```python
import cv2
image = cv2.imread("gpro.jpg")
image = cv2.resize(image, (612, 612))
res = cv2.line(img,(0,0),(612,612),(100,100,205),10)

# Display the HSV image
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/97b1dcd2-b16c-46a7-9552-47efadad7423)

#### 2) Draw a rectangle on the image:
```python
import cv2
image = cv2.imread("gpro.jpg")

# Convert to grayscale
img = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
img = cv2.imread("gpro.jpg")
img = cv2.resize(img, (612, 612))
img.shape
start=(0,0)
stop=(612,612)
color=(100,255,100)
thickness=20

res_img=cv2.rectangle(img,start,stop,color,thickness)

# Display the HSV image
cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4d9e241a-db96-4f0e-afce-3e9c984fc136)

#### 3) Draw a circle on the image:
```python
import cv2
image = cv2.imread("gpro.jpg")
image = cv2.resize(image, (500, 300))
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 60, (0, 255, 0), 5)
cv2.imshow('vinush', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/682f7d74-6693-42a8-99a3-90b1abcf68bc)

#### 4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```python
import cv2
image = cv2.imread("gpro.jpg")
image = cv2.resize(image, (600, 400))
text = "OpenCV Drawing"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('vinush', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/16bbd351-3385-47d8-b2f0-13662ac0bf65)



### iii)Image Color Conversion
#### 1) Convert the image from RGB to HSV and display it
```python
import cv2
image = cv2.imread('gpro.jpg')
image = cv2.resize(image,(600,400))
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/be984cf9-8ace-45be-82c4-1a044e435e47)


#### 2)Convert the image from RGB to GRAY and display it.
```python
import cv2
image = cv2.imread('gpro.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/ec752be5-82b7-4ee2-990e-6607e89122f0)

#### 3)Convert the image from RGB to YCrCb and display it.
```python
import cv2
image = cv2.imread('gpro.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/77e9bb0c-a5d7-46b6-9457-98185264a4a0)


#### 4)Convert the HSV image back to RGB and display it
```python
import cv2
image = cv2.imread('gpro.jpg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/b15f26d2-e0af-4c24-bff3-aa1068eac94d)

### iv)Access and Manipulate Image Pixels

#### 1)Access and print the value of the pixel at coordinates (100, 100)
```python
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/ab57dad3-63f4-4121-bbb8-ff6c8f938c13)

#### 2) Modify the color of the pixel at (200, 200) to white
```python
import cv2
image = cv2.imread('gpro.jpg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4579168f-b559-406d-af56-a665ad2afa82)


### v)Image Resizing
#### Resize the original image to half its size and display it.
```python
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d9e6c558-c293-4ff3-8399-50e9c68009cb)



### vi)Image Cropping
#### Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```python
import cv2
image = cv2.imread('gpro.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4d22e657-2efc-4d29-9e01-f4069885f304)

### vii)Image Flipping
#### 1)Flip the original image horizontally and display it.
```python
import cv2
image = cv2.imread("gpro.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/016e5919-9cb4-4780-b2d0-868de451e1c4)

#### 2)Flip the original image vertically and display it.
```python
import cv2
image = cv2.imread("gpro.jpg")
image = cv2.resize(image,(300,200))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/7be113e7-42cc-4abd-9ede-972153b7c4b0)

### viii)Write and Save the Modified Image
```python
import cv2
img = cv2.imread("gpro.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('mouse.jpg',img)
```

![image](https://github.com/user-attachments/assets/703fd1e3-09ed-4261-8ff7-2a46253843b2)







## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







