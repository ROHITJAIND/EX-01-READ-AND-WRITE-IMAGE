# EX-1 READ AND WRITE AN IMAGE
### AIM:
To write a python program using OpenCV to do the following image manipulations.
- i) Read, display, and write an image.
- ii) Access the rows and columns in an image.
- iii) Cut and paste a small portion of the image.
### Software Required:
- Anaconda - Python 3.7
### Algorithm:
- Step1: Choose an image and save it as a filename.jpg
- Step2: Use imread(filename, flags) to read the file.
- Step3: Use imshow(window_name, image) to display the image.
- Step4: Use imwrite(filename, image) to write the image.
- Step5: End the program and close the output image windows.
### Program:
```
Developed By: ROHIT JAIN D
Register Number: 212222230120
```
#### i) To Read,display the image
```Python
import cv2
image=cv2.imread('blue.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('ROHIT JAIN',image)
cv2.waitKey(0)
cv2.destroyAllWindows() 
```
- Output:<br>
  <img height=20% width=40% src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/8929dcc6-55a7-4b6a-bd48-79ffa35aa244">
#### ii) To write the image
```Python
import cv2
image=cv2.imread('blue.jpg',0)
cv2.imwrite('demo.jpg',image)
```
- Output:<br>
<img height=7% width=50% src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/ee34c455-0e2a-4f8d-b395-df137426399f">

#### iii) Find the shape of the Image
```python3
import cv2
image=cv2.imread('blue.jpg',1)
print(image.shape)
```
- Output:<br>
<img height=7% width=50% src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/c4de6d78-e6e3-4627-8865-a69664f76c32">

#### iv) To access rows and columns

```python3
import random
import cv2
image=cv2.imread('blue.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j] = [random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
- Output:<br>
<img height=20% width=40% src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/1792665b-5d6e-406b-8595-7635378a81a0">

#### v) To cut and paste portion of image
```python3
import cv2
image=cv2.imread('blue.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
- Output:<br>
<img height=20% width=40% src="https://github.com/ROHITJAIND/READ-AND-WRITE-IMAGE/assets/118707073/c409c198-cb71-447e-bd57-a0d138265a2a">

### Result:
Thus the images are read, displayed, and written successfully using the python program.
