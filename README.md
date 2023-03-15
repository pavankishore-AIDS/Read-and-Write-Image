# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:M.Pavan Kishore
### Register Number:212221230076
i) #To Read,display the image
```
 import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('ACE.jpg',1)
cv2_imshow(a)
cv2.waitKey(0) 

```
ii) #To write the image
```
colorImage = cv2.imread('ACE.jpg',1)
cv2.imwrite('ACE.jpg',colorImage)
writtenImage = cv2.imread('ACE.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)


```
iii) #Find the shape of the Image
```python3
colorImage = cv2.imread('ACE.jpg',1)
print(colorImage.shape)


```
iv) #To access rows and columns

```python3
import random
colorImage = cv2.imread('ACE.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)


```
v) #To cut and paste portion of image
```python3
color_img = cv2.imread('luffy.jpeg',1)
tag = color_img[200:400,300:500]
color_img[200:400,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)



```

## Output:

### i) Read and display the image

<br>

<![p1](https://user-images.githubusercontent.com/94154941/225356878-de690fc7-0a66-4da2-b6df-369e521a4ba2.png)
br>

### ii)Write the image

<br>

<![p2](https://user-images.githubusercontent.com/94154941/225356947-6b5cd4d7-e7b6-4eea-ba62-3d0dec47eed5.png)
br>

### iii)Shape of the Image

<br>
![p3](https://user-images.githubusercontent.com/94154941/225357004-fc60d091-b04f-45c8-ac5f-23bb34d0889f.png)

<br>

### iv)Access rows and columns
<br>
![p4](https://user-images.githubusercontent.com/94154941/225357066-88be3ce8-68d4-4d54-8bbb-766dd2cb66e4.png)
<br>

### v)Cut and paste portion of image
<br>
![p5](https://user-images.githubusercontent.com/94154941/225357355-80b6edd4-fd5e-4a15-944f-2d01d3da1dd9.png)

<br>

## Result:
Thus the images are read, displayed, and written successfully using the python program.


