# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: Safeeq Fazil A
### Register Number: 212222240086

## IMAGE

![exp 1 imag](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/8e6f93ad-409c-4fb8-a90f-641badce3aa3)



## Program:

### i) Read and display the image

```
#Read and display the image
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('SAFEEQ FAZIL',image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/b6dc140b-30b3-4069-acc5-4f82e3668046)


### ii)Write the image
```
#Write the image
import cv2
image=cv2.imread('exp1.jpg',0)
cv2.imwrite('demos.jpg',image)
```
## Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/6270d311-ef85-4145-83c1-328cad66dbb0)


### iii)Shape of the Image
```
#Shape of the Image
import cv2
image=cv2.imread('exp1.jpg',1)
print(image.shape)
```

## Output:

![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/caeae6b1-03ff-49b4-ad4d-4af761e481cd)


### iv)Access rows and columns

```
import random
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/f39ab342-4f44-45c9-86ed-3b73539ee5d6)



### v)Cut and paste portion of image
```
#Cut and paste portion of image
import cv2
image=cv2.imread('exp1.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/ca826c0c-4ddf-43a2-a661-ec1dd366455f)


### vi) BGR and RGB to HSV and GRAY
```
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('exp1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Original image:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/dd853d79-d320-4f04-81c9-349926325344)


## Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/5c546600-bb26-44e9-8367-8b834f5496f9)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/ad14a02c-65c4-41a5-b6c6-eb5d758f9939)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/d9cedd42-46b4-40b0-b412-3c654509cb0e)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/0c0b2b0b-2cfc-40d4-aaf4-f3e0bf1129db)



### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('exp1.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Original HSV:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/6debc082-d0f0-42af-a8f8-d3d8255f786c)

##Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/32c9a4ee-d17f-4f21-9cea-8eaa052236e1)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/4978fdd0-1bd4-42b2-a993-299700a470c3)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/537a06fc-1843-44cc-817b-c5473937f060)


### viii) RGB and BGR to YCrCb

```
import cv2
img = cv2.imread('exp1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/dfe74a8d-5f6d-4dec-abea-f1f7c3682524)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/baba940f-c086-4e91-b902-0b0397a08f72)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/a4069e7f-3a12-487a-b790-d7e8f4b79270)


### ix) Split and merge RGB Image

```
#Split and merge RGB Image
import cv2
img = cv2.imread('exp1.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT:
### Channels

![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/8f3fda40-b181-40bd-a924-721123c4008a)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/f48592c4-1a86-4f3d-9468-35dc701deb50)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/17d92fc6-5e69-4c4c-a526-e8755f13588e)

## Merged RGB
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/5564d346-224f-4116-85a8-ce6f4fb1ee45)


### x) Split and merge HSV Image

```
import cv2
img = cv2.imread("exp1.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### merged HSV:

![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/1dd10ff0-149a-4fe2-bd00-b20ae1a2e588)

## splitted
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/72d2c812-69c6-47d7-a4fd-8297ceb8ff44)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/eede3efe-1950-4b4b-a36a-480b10f56181)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/5056a6f4-409f-4559-b3cb-6457b7e6fc44)
![image](https://github.com/Safeeq-Fazil/COLOR_CONVERSIONS_OF-IMAGE/assets/118680361/980118ed-3062-4909-946d-ab37e36219a9)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







